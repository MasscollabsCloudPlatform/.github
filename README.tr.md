# Masscollabs Cloud Platform

Türkçe | [English](README.md)

[Masscollabs Services Masscollabs](https://masscollabs.xyz) tarafından
sürdürülen Masscollabs Cloud Platform için kuruluş genelinde geçerli topluluk
sağlığı ve profil deposu.

## Hakkında

Masscollabs Cloud Platform, [Go programlama dili](https://go.dev) ile
yazılan ve **GNU Affero Genel Kamu Lisansı, sürüm 3 veya (isteğinize bağlı
olarak) sonraki herhangi bir sürüm (AGPL-3.0-or-later)** altında yayımlanan
bir bulut bilişim servisleri ailesidir. Her servis bulut bilişim
senaryoları için geliştirilir ve askeri dayanıklılık seviyesinde kod kalitesi
ile esneklik standardına tabidir.

## Mühendislik İlkeleri

Aşağıdaki ilkeler, bu kuruluştaki kodun kalite çıtasını belirler. Bunlar her
deponun karşılaması ve karşısında denetlenmesi beklenen hedeflerdir.

- **Önce dayanıklılık:** Servisler kısmi arızalara dayanıklı olmalıdır. Her
  ağ sınırında zaman aşımı, bağlam (context) iptali, geri çekilmeli (backoff)
  sınırlı yeniden deneme, devre kesici ve düzgün kapanış kullanın.
- **Varsayılan olarak güvenli:** Tüm girdileri doğrulayın, en az yetki
  ilkesini uygulayın, gizli bilgileri kaynak kodu deposundan uzak tutun ve
  bağımlılıkları asgari, sabitlenmiş ve bilinen güvenlik açıkları için
  taranmış halde tutun (örneğin `govulncheck` ile).
- **Belirleyici kalite kapıları:** Kod birleştirilmeden önce `gofmt`,
  `go vet`, statik analiz (örneğin `staticcheck` veya `golangci-lint`) ve
  yarış dedektörü (`go test -race`) denetimlerinden geçmelidir.
- **Test titizliği:** Değişikliklere birim, entegrasyon, fuzz ve kıyaslama
  (benchmark) testleri eşlik eder; hata yolları başarı yolları kadar
  kapsanır.
- **Gözlemlenebilirlik:** Yapılandırılmış günlükleme, metrikler ve dağıtık
  izleme (örneğin OpenTelemetry) tasarımın parçasıdır, sonradan eklenen bir
  unsur değildir.
- **Tekrarlanabilir derlemeler:** Derlemeler Go modülleri ile sürümlenir;
  tekrarlanabilir ve denetlenebilir olmalıdır.
- **Operasyonel netlik:** Sağlık ve hazır olma uç noktaları, açık
  yapılandırma ve belgelenmiş arıza kipleri zorunludur.

## Lisanslama

Bu kuruluştaki tüm kod AGPL-3.0-or-later ile lisanslanmıştır. AGPL, copyleft
kapsamını ağ üzerinden kullanıma da genişlettiği için, bu servislerin
değiştirilmiş bir sürümünü uzak kullanıcılara sunan herkes, bu kullanıcılara
ilgili kaynak kodunu da sunmak zorundadır. Lisansın tam metni için
[LICENSE](LICENSE) dosyasına bakın.

## Katkıda Bulunma

1. İlgili depoyu çatallayın (fork) ve bir konu dalı oluşturun.
2. Odaklı değişiklikler yapın; testleri ekleyin veya güncelleyin.
3. Yukarıda listelenen kalite kapılarını yerelde çalıştırın.
4. Kullanıcıya görünen değişiklikleri [ChangeLog](ChangeLog) dosyasına
   kaydedin (ABD İngilizcesi ile).
5. Bir çekme isteği (pull request) açın. Katkıda bulunarak çalışmanızın
   AGPL-3.0-or-later ile lisanslanmasını kabul etmiş olursunuz.

## Bağlantılar

- Web sitesi: <https://masscollabs.xyz>

## Lisans

Copyright (C) 2017-2027 Masscollabs Services

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU Affero General Public License as published
by the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU Affero General Public License for more details.

You should have received a copy of the GNU Affero General Public License
along with this program.  If not, see <https://www.gnu.org/licenses/>.
