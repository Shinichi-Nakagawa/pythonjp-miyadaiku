.. article::
   :type: snippet



Python を使って開発や実験を行うときは、用途に応じて専用の実行環境を作成し、切り替えて使用するのが一般的です。こういった、一時的に作成する実行環境を、**「仮想環境」** と言います。

仮想環境は、次のような目的で使われます。

- システム全体で使うPython環境に影響を与えずにモジュールの追加・入れ替えをしたい。

- 同じモジュールの、複数のバージョンを使い分けたい。例えば、開発中のWebアプリケーション開発では、Webアプリケーションフレームワークとして `Django <https://www.djangoproject.com/>`_ の 1.10 を使い、新しいプロジェクトではバージョン 1.11 を使用したい場合など、簡単に切り替えられるようにしたい。

- 異なるバージョンの Python を使いたい。Python2 でしか利用できない、古いモジュールやアプリケーションを使用する場合、Python3.x と Python2.x を切り替えたい。


仮想環境には特定のバージョンのPython本体と、各種モジュールがインストールされます。あるプロジェクトで使用する仮想環境では Python 3.6 と Django 1.11をインストールし、別のプロジェクトの仮想環境には Python 2.7 と Django 1.10 を利用する、といった環境を簡単に構築できます。

仮想環境を作成するモジュールには `Virtualenv <https://virtualenv.pypa.io/en/stable/>`_ と、`venv <https://docs.python.jp/3/library/venv.html>`_ があります。venv は Python3 の標準ライブラリですが、Python2.x で使用することができないため、ここでは Virtualenv を取り上げます。

.. jinja::

   {% if not context.no_virtualenvwrapper %}

また、Virtualenvの管理ツールとして使われることの多い、:jinja:`{{ page.link(fragment='virtualenvwrapper') }}` を紹介します。

.. jinja::

   {% endif %}
