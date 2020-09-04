# Social-Share
partage
# url
    https://pypi.org/project/django-social-share/

# Installation
    pip install django-social-share
# Ajouter au INTALLED_APP
    INSTALLED_APPS += ['django_social_share']
  
# Usage(placer cela dans le html ou devaist se trouver les icons de partage)
    {% post_to_facebook <object_or_url> <link_text> %}

    {% post_to_gplus <object_or_url> <link_text> %}

    {% post_to_twitter <text_to_post> <object_or_url> <link_text> %}

    {% post_to_linkedin <object_or_url> %}

    {% send_email <subject> <text_to_post> <object_or_url> <link_text> %}

    {% post_to_reddit <text_to_post> <object_or_url> <link_text> %}

    {% post_to_telegram <text_to_post> <object_or_url> <link_text> %}

    {% post_to_whatsapp <object_or_url> <link_text> %}
    
    Exemple : 
    {% post_to_facebook object_or_url "Post to Facebook!" %}
    {% post_to_twitter "New Song: {{article.titre}}. Check it out!" object_or_url "Post to Twitter" %}
    {% post_to_telegram "New Song: {{article.titre}}" %}
    {% post_to_whatsapp object_or_url "Share via WhatsApp" %}
    
# Config
    aller dans le venv prendre le dossier django-social-share et le mettre a la racine du dossier templates
    en suite modifier les fichier de chaque reseau social en fonction de son design
    {% load static %}
    Exemple :
    <li>
        <a href="{{ facebook_url }}" target="_blank">
            <div class="icone icone-facebook">
                <img src="{% static 'ressources/icons/facebook.svg' %}" alt="">
            </div>
        </a>
    </li>
