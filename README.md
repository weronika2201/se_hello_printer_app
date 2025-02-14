# Simple Flask App
[![Build status](https://app.statuscake.com/button/index.php?Track=6003152&Days=1&Design=1)](https://app.statuscake.com/UptimeStatus.php?tid=6003152)

[![Build Status](https://travis-ci.com/weronika2201/se_hello_printer_app.svg?branch=master)](https://travis-ci.com/weronika2201/se_hello_printer_app)

Aplikacja Dydaktyczna wyświetlająca imię i wiadomość w różnych formatach dla zajęć
o Continuous Integration, Continuous Delivery i Continuous Deployment.

- W projekcie wykorzystamy virtual environment, dla utworzenia hermetycznego środowisko dla aplikacji:

  ```
  # tworzymy hermetyczne środowisko dla bibliotek aplikacji:
  $ python3 -m venv .venv

  # aktywowanie hermetycznego środowiska
  $ source .venv/bin/activate
  make deps
  $ pip install -r requirements.txt
  $ pip install -r test_requirements.txt

  # zobacz
  $ pip list
  ```

  Sprawdź: [tutorial venv](https://docs.python.org/3/tutorial/venv.html) oraz [biblioteki flask](http://flask.pocoo.org).

- Uruchamianie applikacji:

  ```
  # jako zwykły program
  $ python main.py

  # albo:
  $ PYTHONPATH=. FLASK_APP=hello_world flask run

  #albo za pomoca pliku Makefile:
  $ make run
  ```


- Uruchamianie testów (see: http://doc.pytest.org/en/latest/capture.html):

  ```
  $ PYTHONPATH=. py.test
  $ PYTHONPATH=. py.test --verbose -s
  #albo za pomoca pliku Makefile:
  $ make test
  ```

- Kontynuując pracę z projektem, aktywowanie hermetycznego środowiska dla aplikacji py:

  ```
  # deaktywacja
  $ deactivate
  ```

  ```
  ...

  # aktywacja
  $ source .venv/bin/activate
  ```

- Integracja z TravisCI:


 #miejsce na twoje notatki
  ```

# Pomocnicze

## Ubuntu

- Instalacja dockera: [dockerce howto](https://docs.docker.com/install/linux/docker-ce/ubuntu/)

## Centos

- Instalacja docker-a:

  ```
  $ yum remove docker \
        docker-common \
        container-selinux \
        docker-selinux \
        docker-engine

  $ yum install -y yum-utils

  $ yum-config-manager \
      --add-repo \
      https://download.docker.com/linux/centos/docker-ce.repo

  $ yum makecache fast
  $ yum install -y docker-ce
  $ systemctl start docker
  ```

  #Uptime monitoring statuscake.com
  1 Przejdź do statuscake.com
  2 Utwórz konto.
  3 Dodaj grupę kontaktową ze swoim email-em.
  4 Dodaj Uptime Monitoring test:
  - URL: url Twojej aplikacji
  - Nazwa: dowolna
  - Contact Group: zdefiniowana w 3
  monitoring, który wykryje, kiedy jesteśmy offline



test_cov – wywłanie coverage z wypisaniem raportu na ekran

test_xunit – generacja xunit i coverage
