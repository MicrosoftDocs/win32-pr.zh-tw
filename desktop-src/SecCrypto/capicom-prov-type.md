---
description: 指定密碼編譯服務提供者 (CSP) 的類型。
ms.assetid: faf2390d-bf78-4943-91f3-1db9939fedfb
title: 'CAPICOM_PROV_TYPE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_PROV_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bf85d2eb01ffd4290c5200e09c842f280cd5418dc5203bba068ecb5bcd65c355
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879018"
---
# <a name="capicom_prov_type-enumeration"></a>CAPICOM \_ >prov \_ 類型列舉

**CAPICOM \_ >prov \_ 類型** 列舉會指定 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 的類型。

## <a name="members"></a>成員



| member                             | 描述                                                                                                                                                                                                                                                                                                                                                                        | 值 |
|------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ >PROV \_ RSA \_ FULL**       | 完整的 [*RSA*](../secgloss/r-gly.md) CSP。 此提供者類型支援 [*數位簽章*](../secgloss/d-gly.md) 和資料 [*加密*](../secgloss/e-gly.md)。<br/>                                                            | 1     |
| **CAPICOM \_ >PROV \_ RSA \_ SIG**        | RSA CSP 的子集，僅支援雜湊和數位簽章所需的函數和演算法。<br/>                                                                                                                                                                                                                                        | 2     |
| **CAPICOM \_ >PROV \_ DSS**             | [*數位簽章標準*](../secgloss/d-gly.md) (DSS) CSP。 此提供者類型僅支援雜湊和數位簽章。 DSS 會使用 [*數位簽章演算法*](../secgloss/d-gly.md) (DSA) 。<br/> | 3     |
| **CAPICOM \_ >PROV \_ FORTEZZA**        | 包含密碼編譯通訊協定和演算法的 CSP， (NIST) 的規範 [*標準和技術*](../secgloss/n-gly.md) 。<br/>                                                                                      | 4     |
| **CAPICOM \_ >PROV \_ MS \_ EXCHANGE**    | 針對 Exchange 和其他與 Microsoft Mail 相容之應用程式的密碼編譯需求所設計的 CSP。<br/>                                                                                                                                                                                                                                       | 5     |
| **CAPICOM \_ >PROV \_ SSL**             | 支援 [*安全通訊端層*](../secgloss/s-gly.md) (SSL) 通訊協定的 CSP。<br/>                                                                                                                                                                                              | 6     |
| **CAPICOM \_ >PROV \_ RSA \_ SCHANNEL**   | 支援 [*RSA*](../secgloss/r-gly.md) 和 [*Schannel*](../secgloss/s-gly.md) 通訊協定的 CSP。<br/>                                                                                                                                                                                        | 12    |
| **CAPICOM \_ >PROV \_ DSS \_ DH**         | 支援 DSS 和 [*diffie-hellman*](../secgloss/d-gly.md) 通訊協定的 CSP。<br/>                                                                                                                                                                                                          | 13    |
| **CAPICOM \_ >PROV \_ EC \_ ECDSA \_ SIG**  | 支援橢圓曲線數位簽章演算法的 CSP (ECDSA) 函數和數位簽章所需的演算法。<br/>                                                                                                                                                                                                                                  | 14    |
| **CAPICOM \_ >PROV \_ EC \_ ECNRA \_ SIG**  | 支援橢圓曲線 Nyberg-Rueppel 類比 (ECNRA) 函數和數位簽章所需演算法的 CSP。<br/>                                                                                                                                                                                                                                        | 15    |
| **CAPICOM \_ >PROV \_ EC \_ ECDSA \_ FULL** | 支援完整 ECDSA 的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                   | 16    |
| **CAPICOM \_ >PROV \_ EC \_ ECNRA \_ FULL** | 支援完整 ECNRA 的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                   | 17    |
| **CAPICOM \_ >PROV \_ DH \_ SCHANNEL**    | 支援 [*diffie-hellman*](../secgloss/d-gly.md) 和 [*Schannel*](../secgloss/s-gly.md) 通訊協定的 CSP。<br/>                                                                                                                                   | 18    |
| **CAPICOM \_ >PROV \_ SPYRUS \_ LYNKS**   | 支援 SPYRUS LYNKS 插卡裝置的 CSP。<br/>                                                                                                                                                                                                                                                                                                                     | 20    |
| **CAPICOM \_ >PROV \_ RNG**             | 處理亂數產生的 CSP。<br/>                                                                                                                                                                                                                                                                                                                          | 21    |
| **\_>PROV \_ INTEL \_ SEC 的 CAPICOM**      | 提供 Intel 安全性的 CSP。<br/>                                                                                                                                                                                                                                                                                                                                   | 22    |
| **CAPICOM \_ >PROV \_ 取代 \_ OWF**    | 支援取代從密碼產生單向格式之方法的 CSP。<br/>                                                                                                                                                                                                                                                                  | 23    |
| **CAPICOM \_ >PROV \_ RSA \_ AES**        | 使用進階加密標準 ([*AES*](../secgloss/a-gly.md)) 演算法支援數位簽章和資料加密的 CSP。<br/>                                                                                                                                                                                       | 24    |



## <a name="remarks"></a>備註

下列方法和屬性會使用 **CAPICOM \_ >prov \_ 類型** 列舉：

-   [**PrivateKey. ProviderType**](privatekey-providertype.md) 屬性。
-   [**PrivateKey。 Open**](privatekey-open.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 
