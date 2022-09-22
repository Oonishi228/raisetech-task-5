# 第5回課題
・WEBアプリケーション  
・アプリケーションサーバー  
・Javaのエディションの違い  
・Spring Boot


　上記のことについて調べる。


## WEBアプリケーション
インターネット（WEB）などのネットワークから利用するアプリケーションソフトウェア  
「動的なWEBサイト」(見る人によって表示される内容が違うサイト) のことを指す。  
例「YouTube」「Gmail」「Skype」など


__仕組みと流れ__  
端末（パソコンやスマートフォンなど）   
↓　　　　↑  
WEBサーバー  
↓　　　　↑  
アプリケーションサーバー  
↓　　　　↑  
データベース  


ユーザーが端末のWEBブラウザからインターネットを介してHTTP、HTTPSリクエストを送る。  
WEBサーバーがリクエストを受け取りテキスト情報だけの静的なページであれば、そのままHTML、CSS、画像などのデータをWEBブラウザへ送る（静的なWEBサイト）。動的な処理が必要の場合、アプリケーションサーバーに処理を依頼する。返ってきた処理をデータとして同じくWEBブラウザへ送る。  
アプリケーションサーバーは、WEBサーバから受け付けたリクエストをJavaやPHP、Rubyなどのプログラミング言語を実行して処理する。実行した結果をWEBサーバへと返す。  
データベースでは、WEBサイトに必要なユーザーデータや商品データなどを保存しており、アプリケーションサーバーがアクセスして必要なデータの抽出や加工処理を実行する。  


WEBサーバー、アプリケーションサーバー、データベースの3層構成が、多くのWEBサイトやWEBシステムが採用している。「3階層システム」や「WEB3層構成」などとも呼ばれている。  


・HTTP（Hypertext Transfer Protocol）  
　クライアントサイド（デバイス）とサーバーサイドでやりとりするためのプロトコル（通信ルール）である。  
・HTTPS（Hytertext Transfer Protocol Secure）  
　HTTPを暗号化をして通信を安全に行うための仕組み。ネットバンキング、クレジットカード決済サービス、個人情報登録や編集を行うようなケースでHTTPSが利用されている。


 ## アプリケーションサーバー  
 WEBサーバより受け取った情報を処理するためのモノ。プログラミング言語（Java、Ruby、PHPなど）で構築されたアプリを実行して、動的なコンテンツを生成している。データベースへのアクセス制御、セキュリティ管理、ユーザー認証処理などの動的な処理機能が搭載されている。  
 アプリケーションサーバの代表的な種類としてTomcat（Java)・Apache (PHP)・Unicorn（Ruby）などがある。  
 
 
__Tomcat__  
プログラミング言語Javaにおいて利用されるアプリケーションサーバーの一種。
Webアプリケーション実行環境においてJavaサーブレット（JavaでWEBアプリケーションを構築する際に作成するクラスを指す）を用いた動的なコンテンツを生成します。正式名称はApache Tomcat。  


__Apache__  
正式名称はApache HTTP Server（アパッチ エイチティーティーピー サーバー）。WEBサーバーの一種。mod_phpというモジュールを追加することで、PHPのアプリケーションサーバーとして利用できる。  


__Unicorn__  
プログラミング言語Rubyにおいて利用されるアプリケーションサーバーの一種。  


## Javaのエディションの違い
__Java SE__  
Java Platform, Standard Editionの略で、Javaで使用されるAPIをまとめたもの。  
APIとはApplication Programming Interfaceの略で、この場合はJavaの機能やデータなどを利用するための呼び出し方を定義したもの。  
非常に多いAPIの中でも基本となるAPIをまとめたのがJava SE


__Java EE__  
Java Platform, Enterprise Editionの略で大規模なシステムを開発する場合に必要となるAPIが含まれる。  
Java EEは、Java SEの拡張機能という位置付け、使用する場合はJava SEと合わせて使用する。  


__Java ME__  
Java Platform, Micro Editionの略。家電などの組み込み機器やモバイルデバイスで動作するアプリケーションを開発するために使用するAPIがまとめられたもの。  


## Spring Boot
Spring Frameworkプロジェクト群を凡庸性のある形でパッケージ化し、シンプルに誰にでも活用できるようにしたフレームワーク。


・Spring Framework  
　JavaのWEBフレームワークの一つ。修正や変更などに強い、テストが簡単、拡張性が高い、保守性が高い、再利用性が高い。など従来のWebアプリケーションにおける様々な問題を解決しており、非常に有力なフレームワークとして、長い間注目されてきている。  
・フレームワーク  
　アプリケーションの標準構造を実装するのに使われるクラスや、ライブラリ（凡庸性の高い複数のプログラムを一つにまとめたもの）の集まり。アプリ開発をする際に、開発の効率を上げる便利な機能がたくさん詰まったツール。


Spring Frameworkが提供する機能の数は多く、実現できることが多い反面、開発プロジェクトへの導入・Java初学者の勉強へのハードルが高くなることにつながった。Spring Bootは、こうしたデメリットを解消する。


__Spring Bootの利点__  
Tomcatが初めから組み込まれている。  
JavaでのWEBシステム開発は、warファイルを作りTomcatやJBossなどのアプリケーションサーバーにデプロイするのが一般的。Spring BootではTomcatが初めから組み込まれているため、普通のJavaファイルと同じようにJavaクラスを起動すると、Tomcatも自動で起動してアプリケーションが勝手にデプロイされて動くようになる。


xmlファイルの記述が不要  
Spring Frameworkで用意されている多種多様な機能を使うためには、xmlファイルに必要なプロジェクト・ライブラリを記載していき適切な設定を記載していく必要がある。一文字でも間違えるとプロジェクトが起動できない。Spring Bootでは、この設定ファイル作成・記述という複雑な作業をできる限り排除してくれる。


・xmlファイル  
　ファイル名の拡張子が「.xml」のファイルで、XML（Extensible Markup Language）で記述されたテキストファイルのこと。XMLはマークアップ言語を定義することができる。マークアップ言語とは「WEBサイト文章といったテキストに目印付けを行い、コンピューターに認識させるための言語」。文章の意味合いを「タグ」と呼ばれる要素で記述して分類し、装飾を行う。
 

## 追加課題
__RESTful APIとは__   
・RESTとは、「REpresentational State Transfer」の略。クライアントとサーバ間でデータをやりとりするアプリケーションを構築するためのアーキテクチャスタイル（複数の基本設計に共通する性質、様式、作法あるいは流儀を指す言葉）の一つ。RESTのアーキテクチャスタイルには、いくつかの重要な原則があり、これらの原則に従っているもの(システムなど)は RESTfulと表現される。  
・「統一インターフェース」「アドレス可能性」「接続性」「ステートレス性」の、RESTの4原則に則ったAPIをREST API （RESTful API） と呼ぶ。  
・RESTful Web Serviceで、データベースなどで管理している情報の中からクライアントに提供すべき情報を「リソース」として抽出し、抽出した「リソース」に対するCRUD操作をHTTPメソッド(POST/GET/PUT/DELETE)を使ってクライアントに提供する。「リソース」に対するCRUD操作は「REST API」や「RESTful API」と呼ばれる。  
・標準的なウェブライブラリやツールを使って呼び出すことができる HTTP サービス。  
・RESTful Web サービスとの対話を可能にするアプリケーション・プログラミング・インタフェース (API または Web API)   


__HTTPリクエストメソッド__  
・GET  
　指定したリソースの表現をリクエストする。GETを使用するリクエストは、データの取り込みに限る。  
・POST  
　指定したリソースに実体を送信するために使用するメソッド。サーバー上の状態を変更したり、副作用が発生したりすることがよくある。  
・PUT  
　対象リソースの現在の表現全体を、リクエストのペイロード（ヘッダを除いた通信本体）で置き換える。  
・PATCH  
　リソースを部分的に変更するために使用する。  
・DELETE  
　指定したリソースを削除する。  
 
 
 __HTTPレスポンスのステータスコード__  
・200  
　リクエストが成功したことを示す。HTTP メソッドにより成功の意味が異なる。  
 　・GET：リソースが読み込まれ、メッセージ本文で転送された。  
 　・HEAD：メッセージ本文がなく、表現ヘッダーがレスポンスに含まれている。  
 　・PUTまたはPOST：操作の結果を表すリソースがメッセージ本文で送信される。  
 　・TRACE：メッセージ本文に、サーバーが受け取ったリクエストメッセージが含まれている。  
・201  
　リクエストは成功し、その結果新たなリソースが作成されたことを示す。POSTリクエストや、一部のPUTリクエストを送信した後のレスポンスになる。  
・500  
　サーバー側で処理方法がわからない事態が発生したことを示す。  
・400  
　構文が無効であるためサーバーがリクエストを理解できないことを示す。  
・404  
　・サーバーがリクエストされたリソースを発見できないことを示す。  
　・ブラウザーでは、これはURLが解釈できなかったことを意味する。  
　・APIでは、これは通信先が有効であるものの、リソース自体が存在しないことを意味することがある。  
　・サーバーは認証されていないクライアントからリソースの存在を隠すために、403の代わりにこのレスポンスを返すことがある。  
 　おそらくもっとも有名なコード。  
  
  
### 201の際にレスポンスヘッダーにLocationヘッダーを設定  
リクエストが成功  
↓  
レスポンスヘッダーに設定されているLocationヘッダーへ  
↓  
LocationヘッダーにはURLが記載されており、ここに設定されたURLに自動的にリダイレクトされる。  
↓  
設定されたURLのブラウザが開く。


HTTPレスポンスは、ステータスライン、レスポンスヘッダー、レスポンスボディの三つの構造でできている。  
・ステータスライン：HTTPリクエストの結果が、「HTTPのバージョン ステータスコード ステータスコードの説明」で返ってくる。例　HTTP/1.1 200 OK  
・レスポンスヘッダー：ステータスラインに書ききれない情報が「フィールド名：内容」書かれてる。サーバーはどこか、レスポンスした時間など。  
・レスポンスボディ：HTMLファイルの中身。リクエストされたファイルの中身が書いてある。  


Locationヘッダー  
　・HTTPレスポンスのレスポンスコードが302などリダイレクトを示すものである場合、自動的にリダイレクトを行う。このとき、リダイレクトを行う先の情報として利用されるのが、レスポンスヘッダーのLocationヘッダーである。  
　・__Locationヘッダーには、ブラウザが次にアクセスすべきURLが記載されており、実際にユーザーのブラウザ上に表示されるコンテンツは、Locationヘッダーに記載されたURLとなる。ここに設定されたURLに自動的にリダイレクトされるということ。__


201 Created → リクエストが成功してリソースの作成が完了したことを表す。レスポンスが返される前に、新たなリソースが作成され、レスポンスメッセージの本文にて新しいリソースが返される。__その位置はリクエスト URL、または Locationヘッダーの内容となる。__  


※Locationヘッダーに設定される値は、RFCで「値は単一の絶対URIで構成される。」と定義されているため、URL以外は認められない。  
 ・RFC（Request For Comment）インターネット技術の標準を定める「IETF」が正式に発行する文書であり、国際的なインターネット技術の決まり事(使用・要件)がさだめられている。
