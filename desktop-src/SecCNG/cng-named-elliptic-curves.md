---
description: 從 Windows 10 開始，CNG 提供下列命名橢圓曲線的支援 (ANSI x x9.62、x 9.63、FIPS 186-2) 。
ms.assetid: 0607E8C3-6372-47E1-B16F-EF156D5EBA7D
title: CNG 命名橢圓曲線 (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 691f1211b56abc41d622d20857653723be37681014a9bf72b91c1384c8f4b8cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908249"
---
# <a name="cng-named-elliptic-curves"></a>CNG 命名橢圓曲線

從 Windows 10 開始，CNG 提供下列命名橢圓曲線的支援 (ANSI x x9.62、x 9.63、FIPS 186-2) 。

<dl> <dt><span id="BCRYPT_ECC_CURVE_25519"></span><span id="bcrypt_ecc_curve_25519"></span>**BCRYPT \_ ECC \_ 曲線 \_ 25519**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------|
| 名稱              | curve25519                                                  |
| 標準          | [曲線25519](https://cr.yp.to/ecdh/curve25519-20060209.pdf) |
| 金鑰大小 (位元)   | 255                                                         |
| 支援 TLS       |                                                             |
| 物件識別碼 | 無                                                        |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160R1"></span><span id="bcrypt_ecc_curve_brainpoolp160r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP160R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP160r1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 160                                                                                                               |
| 支援 TLS       | No                                                                                                                |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.1                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP160T1_"></span><span id="bcrypt_ecc_curve_brainpoolp160t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ BRAINPOOLP160T1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP160t1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 160                                                                                                               |
| 支援 TLS       | No                                                                                                                |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.2                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192R1"></span><span id="bcrypt_ecc_curve_brainpoolp192r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP192R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP192r1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 192                                                                                                               |
| 支援 TLS       | No                                                                                                                |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.3                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP192T1"></span><span id="bcrypt_ecc_curve_brainpoolp192t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP192T1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP192t1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 192                                                                                                               |
| 支援 TLS       | No                                                                                                                |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.4                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224R1"></span><span id="bcrypt_ecc_curve_brainpoolp224r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP224R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP224r1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 224                                                                                                               |
| 支援 TLS       | No                                                                                                                |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.5                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP224T1"></span><span id="bcrypt_ecc_curve_brainpoolp224t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP224T1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP224t1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 224                                                                                                               |
| 支援 TLS       | No                                                                                                                |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.6                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256R1"></span><span id="bcrypt_ecc_curve_brainpoolp256r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP256R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP256r1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 256                                                                                                               |
| 支援 TLS       | Yes                                                                                                               |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.7                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP256T1"></span><span id="bcrypt_ecc_curve_brainpoolp256t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP256T1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP256t1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 256                                                                                                               |
| 支援 TLS       | No                                                                                                                |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.8                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP320R1"></span><span id="bcrypt_ecc_curve_brainpoolp320r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP320R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP320r1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 320                                                                                                               |
| 支援 TLS       | No                                                                                                                |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.9                                                                                              |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP32_0T1"></span><span id="bcrypt_ecc_curve_brainpoolp32_0t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP32 0T1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP320t1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 320                                                                                                               |
| 支援 TLS       | No                                                                                                                |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.10                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384R1_"></span><span id="bcrypt_ecc_curve_brainpoolp384r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ BRAINPOOLP384R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP384r1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 384                                                                                                               |
| 支援 TLS       | Yes                                                                                                               |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.11                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP384T1"></span><span id="bcrypt_ecc_curve_brainpoolp384t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP384T1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP384t1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 384                                                                                                               |
| 支援 TLS       | No                                                                                                                |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.12                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512R1"></span><span id="bcrypt_ecc_curve_brainpoolp512r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP512R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP512r1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 512                                                                                                               |
| 支援 TLS       | Yes                                                                                                               |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.13                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_BRAINPOOLP512T1"></span><span id="bcrypt_ecc_curve_brainpoolp512t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ BRAINPOOLP512T1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------------------------------------|
| 名稱              | brainpoolP512t1                                                                                                   |
| 標準          | [ECC Brainpool 標準曲線和曲線產生](https://www.teletrust.de/fileadmin/files/oid/oid_ECC-Brainpool-Standard-curves-V1.pdf) |
| 金鑰大小 (位元)   | 512                                                                                                               |
| 支援 TLS       | No                                                                                                                |
| 物件識別碼 | 1.3.36.3.3.2.8.1.1.14                                                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_EC192WAPI_"></span><span id="bcrypt_ecc_curve_ec192wapi_"></span>**BCRYPT \_ECC \_ 曲線 \_ EC192WAPI**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|----------------------------------------------------------------|
| 名稱              | ec192wapi                                                      |
| 標準          | 國際區域網路的中文標準 (GB 15629.11-2003)  |
| 金鑰大小 (位元)   | 192                                                            |
| 支援 TLS       | No                                                             |
| 物件識別碼 | 1.2.156.11235.1.1.2.1                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP192"></span><span id="bcrypt_ecc_curve_nistp192"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP192**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| 名稱              | nistP192                                                                                                                     |
| 標準          | [聯邦政府使用的建議橢圓曲線](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| 金鑰大小 (位元)   | 192                                                                                                                          |
| 支援 TLS       | Yes                                                                                                                          |
| 物件識別碼 | 1.2.840.10045.3.1.1                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP224_"></span><span id="bcrypt_ecc_curve_nistp224_"></span>**BCRYPT \_ECC \_ 曲線 \_ NISTP224**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| 名稱              | nistP224                                                                                                                     |
| 標準          | [聯邦政府使用的建議橢圓曲線](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| 金鑰大小 (位元)   | 224                                                                                                                          |
| 支援 TLS       | Yes                                                                                                                          |
| 物件識別碼 | 1.3.132.0.33                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP256"></span><span id="bcrypt_ecc_curve_nistp256"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP256**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| 名稱              | nistP256                                                                                                                     |
| 標準          | [聯邦政府使用的建議橢圓曲線](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| 金鑰大小 (位元)   | 256                                                                                                                          |
| 支援 TLS       | Yes                                                                                                                          |
| 物件識別碼 | 1.2.840.10045.3.1.7                                                                                                          |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP384_"></span><span id="bcrypt_ecc_curve_nistp384_"></span>**BCRYPT \_ECC \_ 曲線 \_ NISTP384**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| 名稱              | nistP384                                                                                                                     |
| 標準          | [聯邦政府使用的建議橢圓曲線](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| 金鑰大小 (位元)   | 384                                                                                                                          |
| 支援 TLS       | Yes                                                                                                                          |
| 物件識別碼 | 1.3.132.0.34                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NISTP521"></span><span id="bcrypt_ecc_curve_nistp521"></span>**BCRYPT \_ ECC \_ 曲線 \_ NISTP521**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------------------------------------------|
| 名稱              | nistP521                                                                                                                     |
| 標準          | [聯邦政府使用的建議橢圓曲線](https://csrc.nist.gov/groups/ST/toolkit/documents/dss/NISTReCur.pdf) |
| 金鑰大小 (位元)   | 521                                                                                                                          |
| 支援 TLS       | Yes                                                                                                                          |
| 物件識別碼 | 1.3.132.0.35                                                                                                                 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP256T1_"></span><span id="bcrypt_ecc_curve_numsp256t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ NUMSP256T1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 名稱              | numsP256t1                                                                                                                              |
| 標準          | [MSR ECCLib 中的曲線選取和支援曲線參數規格](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| 金鑰大小 (位元)   | 256                                                                                                                                     |
| 支援 TLS       | No                                                                                                                                      |
| 物件識別碼 | 無                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP384T1_"></span><span id="bcrypt_ecc_curve_numsp384t1_"></span>**BCRYPT \_ECC \_ 曲線 \_ NUMSP384T1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 名稱              | numsP384t1                                                                                                                              |
| 標準          | [MSR ECCLib 中的曲線選取和支援曲線參數規格](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| 金鑰大小 (位元)   | 384                                                                                                                                     |
| 支援 TLS       | No                                                                                                                                      |
| 物件識別碼 | 無                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_NUMSP512T1"></span><span id="bcrypt_ecc_curve_numsp512t1"></span>**BCRYPT \_ ECC \_ 曲線 \_ NUMSP512T1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| 名稱              | numsP512t1                                                                                                                              |
| 標準          | [MSR ECCLib 中的曲線選取和支援曲線參數規格](https://research.microsoft.com/pubs/219966/curvegen.pdf) |
| 金鑰大小 (位元)   | 512                                                                                                                                     |
| 支援 TLS       | No                                                                                                                                      |
| 物件識別碼 | 無                                                                                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160K1_"></span><span id="bcrypt_ecc_curve_secp160k1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160K1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 名稱              | secP160k1                                                                       |
| 標準          | [建議的橢圓曲線網域參數](https://www.secg.org/sec2-v2.pdf) |
| 金鑰大小 (位元)   | 160                                                                             |
| 支援 TLS       | Yes                                                                             |
| 物件識別碼 | 1.3.132.0.9                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 名稱              | secP160r1                                                                       |
| 標準          | [建議的橢圓曲線網域參數](https://www.secg.org/sec2-v2.pdf) |
| 金鑰大小 (位元)   | 160                                                                             |
| 支援 TLS       | Yes                                                                             |
| 物件識別碼 | 1.3.132.0.8                                                                     |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP160R1_"></span><span id="bcrypt_ecc_curve_secp160r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP160R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 名稱              | secP160r2                                                                       |
| 標準          | [建議的橢圓曲線網域參數](https://www.secg.org/sec2-v2.pdf) |
| 金鑰大小 (位元)   | 160                                                                             |
| 支援 TLS       | Yes                                                                             |
| 物件識別碼 | 1.3.132.0.30                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192K1"></span><span id="bcrypt_ecc_curve_secp192k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP192K1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 名稱              | secP192k1                                                                       |
| 標準          | [建議的橢圓曲線網域參數](https://www.secg.org/sec2-v2.pdf) |
| 金鑰大小 (位元)   | 192                                                                             |
| 支援 TLS       | Yes                                                                             |
| 物件識別碼 | 1.3.132.0.31                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP192R1_"></span><span id="bcrypt_ecc_curve_secp192r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP192R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 名稱              | secP192r1                                                                       |
| 標準          | [建議的橢圓曲線網域參數](https://www.secg.org/sec2-v2.pdf) |
| 金鑰大小 (位元)   | 192                                                                             |
| 支援 TLS       | Yes                                                                             |
| 物件識別碼 | 1.2.840.10045.3.1.1                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224K1"></span><span id="bcrypt_ecc_curve_secp224k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP224K1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 名稱              | secP224k1                                                                       |
| 標準          | [建議的橢圓曲線網域參數](https://www.secg.org/sec2-v2.pdf) |
| 金鑰大小 (位元)   | 224                                                                             |
| 支援 TLS       | Yes                                                                             |
| 物件識別碼 | 1.3.132.0.32                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP224R1"></span><span id="bcrypt_ecc_curve_secp224r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP224R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 名稱              | secP224r1                                                                       |
| 標準          | [建議的橢圓曲線網域參數](https://www.secg.org/sec2-v2.pdf) |
| 金鑰大小 (位元)   | 224                                                                             |
| 支援 TLS       | Yes                                                                             |
| 物件識別碼 | 1.3.132.0.33                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256K1"></span><span id="bcrypt_ecc_curve_secp256k1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP256K1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 名稱              | secP256k1                                                                       |
| 標準          | [建議的橢圓曲線網域參數](https://www.secg.org/sec2-v2.pdf) |
| 金鑰大小 (位元)   | 256                                                                             |
| 支援 TLS       | Yes                                                                             |
| 物件識別碼 | 1.3.132.0.10                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP256R1"></span><span id="bcrypt_ecc_curve_secp256r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP256R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 名稱              | secP256r1                                                                       |
| 標準          | [建議的橢圓曲線網域參數](https://www.secg.org/sec2-v2.pdf) |
| 金鑰大小 (位元)   | 256                                                                             |
| 支援 TLS       | Yes                                                                             |
| 物件識別碼 | 1.2.840.10045.3.1.7                                                             |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP384R1_"></span><span id="bcrypt_ecc_curve_secp384r1_"></span>**BCRYPT \_ECC \_ 曲線 \_ SECP384R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 名稱              | secP384r1                                                                       |
| 標準          | [建議的橢圓曲線網域參數](https://www.secg.org/sec2-v2.pdf) |
| 金鑰大小 (位元)   | 384                                                                             |
| 支援 TLS       | Yes                                                                             |
| 物件識別碼 | 1.3.132.0.34                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_SECP521R1"></span><span id="bcrypt_ecc_curve_secp521r1"></span>**BCRYPT \_ ECC \_ 曲線 \_ SECP521R1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------|
| 名稱              | secP521r1                                                                       |
| 標準          | [建議的橢圓曲線網域參數](https://www.secg.org/sec2-v2.pdf) |
| 金鑰大小 (位元)   | 521                                                                             |
| 支援 TLS       | Yes                                                                             |
| 物件識別碼 | 1.3.132.0.35                                                                    |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS12"></span><span id="bcrypt_ecc_curve_wtls12"></span>**BCRYPT \_ ECC \_ 曲線 \_ WTLS12**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|--------------|
| 名稱              | wtls12       |
| 標準          | WTLS         |
| 金鑰大小 (位元)   | 224          |
| 支援 TLS       | No           |
| 物件識別碼 | 1.3.132.0.33 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS7"></span><span id="bcrypt_ecc_curve_wtls7"></span>**BCRYPT \_ ECC \_ 曲線 \_ WTLS7**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|--------------|
| 名稱              | wtls7        |
| 標準          | WTLS         |
| 金鑰大小 (位元)   | 160          |
| 支援 TLS       | No           |
| 物件識別碼 | 1.3.132.0.30 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_WTLS9_"></span><span id="bcrypt_ecc_curve_wtls9_"></span>**BCRYPT \_ECC \_ 曲線 \_ WTLS9**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------|
| 名稱              | wtls9         |
| 標準          | WTLS          |
| 金鑰大小 (位元)   | 160           |
| 支援 TLS       | No            |
| 物件識別碼 | 2.23.43.1.4.9 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V1"></span><span id="bcrypt_ecc_curve_x962p192v1"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P192V1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------|
| 名稱              | x962P192v1          |
| 標準          | ANSI X X9.62          |
| 金鑰大小 (位元)   | 192                 |
| 支援 TLS       | No                  |
| 物件識別碼 | 1.2.840.10045.3.1.1 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V2_"></span><span id="bcrypt_ecc_curve_x962p192v2_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P192V2**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------|
| 名稱              | x962P192v2          |
| 標準          | ANSI X X9.62          |
| 金鑰大小 (位元)   | 192                 |
| 支援 TLS       | No                  |
| 物件識別碼 | 1.2.840.10045.3.1.2 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P192V3"></span><span id="bcrypt_ecc_curve_x962p192v3"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P192V3**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------|
| 名稱              | x962P192v3          |
| 標準          | ANSI X X9.62          |
| 金鑰大小 (位元)   | 192                 |
| 支援 TLS       | No                  |
| 物件識別碼 | 1.2.840.10045.3.1.3 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V1_"></span><span id="bcrypt_ecc_curve_x962p239v1_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------|
| 名稱              | x962P239v1          |
| 標準          | ANSI X X9.62          |
| 金鑰大小 (位元)   | 239                 |
| 支援 TLS       | No                  |
| 物件識別碼 | 1.2.840.10045.3.1.4 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V2_"></span><span id="bcrypt_ecc_curve_x962p239v2_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V2**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------|
| 名稱              | x962P239v2          |
| 標準          | ANSI X X9.62          |
| 金鑰大小 (位元)   | 239                 |
| 支援 TLS       | No                  |
| 物件識別碼 | 1.2.840.10045.3.1.5 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P239V3_"></span><span id="bcrypt_ecc_curve_x962p239v3_"></span>**BCRYPT \_ECC \_ 曲線 \_ X962P239V3**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------|
| 名稱              | x962P239v3          |
| 標準          | ANSI X X9.62          |
| 金鑰大小 (位元)   | 239                 |
| 支援 TLS       | No                  |
| 物件識別碼 | 1.2.840.10045.3.1.6 |



 

</dt> </dl> </dd> <dt><span id="BCRYPT_ECC_CURVE_X962P256V1"></span><span id="bcrypt_ecc_curve_x962p256v1"></span>**BCRYPT \_ ECC \_ 曲線 \_ X962P256V1**</dt> <dd> <dl> <dt> 

| 需求 | 值 |
|-------------------|---------------------|
| 名稱              | x962P256v1          |
| 標準          | ANSI X X9.62          |
| 金鑰大小 (位元)   | 256                 |
| 支援 TLS       | No                  |
| 物件識別碼 | 1.2.840.10045.3.1.7 |



 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>備註

若要使用命名曲線，請使用 **BCRYPT \_ ECDSA \_ 演算法** 或 **BCRYPT \_ ECDH \_ 演算法** 來呼叫 [**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider) ，作為演算法識別碼。 然後，呼叫 [**BCryptSetProperty**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptsetproperty) ，並將 [ **BCRYPT \_ ECC \_ 曲線 \_ 名稱** ] 屬性設定為上述其中一個曲線或任何已在電腦上註冊的命名曲線，如命令所示 `certutil -displayEccCurve` 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Bcrypt。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**BCryptOpenAlgorithmProvider**](/windows/win32/api/Bcrypt/nf-bcrypt-bcryptopenalgorithmprovider)
</dt> <dt>

[**NCryptCreatePersistedKey**](/windows/win32/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey)
</dt> </dl>

 

 




