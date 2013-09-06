.. Requests documentation master file, created by
   sphinx-quickstart on Sun Feb 13 23:54:25 2011.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

Requests: хумани HTTP
======================

Издање v\ |version|. (:ref:`Installation <install>`)

Requests је :ref:`Apache2 Licensed <apache2>` HTTP библиотека, написана на програмском језику Python, за обичне смртнике.

Python-ов стандардни **urllib2** модул обезбјеђује већину онога што вам је потребно у вези са HTTP-ом, 
али је API поприлично **џомбаст**.
Направљен је за друго вријеме и другачији веб. Захтјева *претјерану* количину рада (па и уз „overrides”) за
обављање најпростијих задатака.

Ствари не би требале да су такве... бар не кад је Python у питању.

::

    >>> r = requests.get('https://api.github.com/user', auth=('user', 'pass'))
    >>> r.status_code
    200
    >>> r.headers['content-type']
    'application/json; charset=utf8'
    >>> r.encoding
    'utf-8'
    >>> r.text
    u'{"type":"User"...'
    >>> r.json()
    {u'private_gists': 419, u'total_private_repos': 77, ...}

Погледати `сличан код, који не користи Requests <https://gist.github.com/973705>`_.

Requests износи сав посао изван HTTP/1.1 — чинећи вашу интеграцију са веб сервисима seamless. Нема потребе за
мануелним додавањем (знаковних) ниски захтјева вашим URL-овима, или да form-encode ваше POST податке. 
Keep-alive и обједињавање HTTP конекција је 100% аутоматско, потпомогнуто библиотеком `urllib3 <https://github.com/shazow/urllib3>`_, који је усађен у Requests.


Свједочења
----------

Her Majesty's Government, Amazon, Google, Twilio, Mozilla, Heroku, PayPal, NPR, Obama for America, Transifex, Native Instruments, The Washington Post, Twitter, SoundCloud, Kippt, Readability, and Federal US Institutions use Requests internally. It has been downloaded over 3,000,000 times from PyPI.

**Armin Ronacher**
    Requests is the perfect example how beautiful an API can be with the
    right level of abstraction.

**Matt DeBoard**
    I'm going to get @kennethreitz's Python requests module tattooed
    on my body, somehow. The whole thing.

**Daniel Greenfeld**
    Nuked a 1200 LOC spaghetti code library with 10 lines of code thanks to
    @kennethreitz's request library. Today has been AWESOME.

**Kenny Meyers**
    Python HTTP: When in doubt, or when not in doubt, use Requests. Beautiful,
    simple, Pythonic.


Feature Support
---------------

Requests is ready for today's web.

- Међународни домени и URL-ови
- Keep-Alive & Connection Pooling
- Сесије уз Cookie Persistence
- Прегледнички (browser-ски) стил SSL верификације
- Basic/Digest Authentication
- Елегантни Кључ/Вриједност Колачићи
- Аутоматска декомпресија
- Unicode Response Bodies
- Отпремање вишедјелних датотека
- Connection Timeouts
- ``.netrc`` support
- Python 2.6—3.3
- Thread-safe.


Водич за кориснике
------------------

Овај, углавном прозаични, дио документације приказује неке од основих могућности библиотеке Requests, 
а онда се постепеним, корак-по-корак упутствима, фокусира за максимално искоришћавање могћности Requests-a.

.. toctree::
   :maxdepth: 2

   user/intro
   user/install
   user/quickstart
   user/advanced
   user/authentication


Водич за заједницу
------------------

Овај, углавном прозаични, дио документације, разматра детаље 
Requests заједнице и својеврсног екосистема.

.. toctree::
   :maxdepth: 1

   community/faq
   community/out-there.rst
   community/support
   community/updates

API документација
-----------------

Уколико тражите неке информације о конкретној функцији, класи или методу,
овај дио документације је за вас.

.. toctree::
   :maxdepth: 2

   api


Водич за сараднике
------------------

Ако желите допринијети пројекту, овај дио документације је за вас.

.. toctree::
   :maxdepth: 1

   dev/philosophy
   dev/internals
   dev/todo
   dev/authors
