---
title: MicrosoftDNS_SIGType 類別
description: MicrosoftDNS ResourceRecord 的子類別 \_ ，表示 (SIG) 資源記錄的簽章。
ms.assetid: ef3729ad-448b-449e-ae59-34888925128a
keywords:
- MicrosoftDNS_SIGType 類別 DNS
- MicrosoftDNS_SIGType 類別 DNS，說明
topic_type:
- apiref
api_name:
- MicrosoftDNS_SIGType
- MicrosoftDNS_SIGType.CreateInstanceFromPropertyData
- MicrosoftDNS_SIGType.Modify
- MicrosoftDNS_SIGType.TypeCovered
- MicrosoftDNS_SIGType.Algorithm
- MicrosoftDNS_SIGType.Labels
- MicrosoftDNS_SIGType.OriginalTTL
- MicrosoftDNS_SIGType.SignatureExpiration
- MicrosoftDNS_SIGType.SignatureInception
- MicrosoftDNS_SIGType.KeyTag
- MicrosoftDNS_SIGType.SignerName
- MicrosoftDNS_SIGType.Signature
api_location:
- Root\MicrosoftDNS
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 172869e90664f88e53fc4cfc89f23b8adbf1e3a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685598"
---
# <a name="microsoftdns_sigtype-class"></a>MicrosoftDNS \_ SIGType 類別

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)的子類別，表示 (SIG) 資源記錄的簽章。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
class MicrosoftDNS_SIGType : MicrosoftDNS_ResourceRecord
{
  uint16 TypeCovered;
  uint16 Algorithm;
  uint16 Labels;
  uint32 OriginalTTL;
  uint32 SignatureExpiration;
  uint32 SignatureInception;
  uint16 KeyTag;
  string SignerName;
  string Signature;
};
```

## <a name="members"></a>成員

**MicrosoftDNS \_ SIGType** 類別具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**MicrosoftDNS \_ SIGType** 類別具有這些方法。



| 方法                             | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|:-----------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CreateInstanceFromPropertyData** | 根據方法的輸入參數中的資料具現化 SIG RR：記錄的 DNS 伺服器名稱、容器名稱、擁有者名稱、類別 (預設值 = IN) 、存留時間值，以及 WINS 對應旗標、反向查閱超時、WINS 快取超時和要附加的功能變數名稱。 它會將新物件的參考傳回做為輸出參數。 <br/> 限定詞：實作為、靜態<br/>                                                                                                                                                                                                                                                       |
| **修改**                         | 將 TTL、對應旗標、查閱超時、快取超時和結果網域更新為指定為此方法之輸入參數的值。 如果未指定參數的新值，則不會變更參數的目前值。 方法會將修改過之物件的參考傳回為輸出參數。 <br/> 限定詞：實作為<br/> **Windows Server 2003：** 這個方法也會將 TypeCovered、演算法、標籤、OriginalTTL、SignatureExpiration、SignatureInception、KeyTag、SignerName 和簽章更新為指定為此方法之輸入參數的值。<br/> <br/> |



 

### <a name="properties"></a>屬性

**MicrosoftDNS \_ SIGType** 類別具有這些屬性。

<dl> <dt>

**演算法**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

與資源記錄中指定的金鑰搭配使用的演算法。 指派的值如下表所示。



| 值                                                                                                | 意義                                |
|------------------------------------------------------------------------------------------------------|----------------------------------------|
| <span id="1"></span><dl> <dt>**1**</dt> </dl> | RSA/MD5 (RFC 2537) <br/>          |
| <span id="2"></span><dl> <dt>**2**</dt> </dl> | Diffie-Hellman (RFC 2539) <br/>   |
| <span id="3"></span><dl> <dt>**3**</dt> </dl> | DSA (RFC 2536) <br/>              |
| <span id="4"></span><dl> <dt>**4**</dt> </dl> | 橢圓曲線密碼編譯<br/> |



 

</dd> <dt>

**KeyTag**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

方法，用來選擇驗證 SIG 的索引鍵。 如需用來計算 KeyTag 的方法，請參閱 RFC 2535、附錄 C。

</dd> <dt>

**標籤**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

原始 SIG RR 擁有者名稱中的標籤計數（不帶正負號）。 此計數不包含根的 Null 標籤，也不包含任何初始萬用字元。

</dd> <dt>

**OriginalTTL**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

由 SIG 簽署之 RR 集合的 TTL。

</dd> <dt>

**簽名**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

以 base 64 表示的簽章，格式如 RFC 2535 中所定義，附錄 A。

</dd> <dt>

**SignatureExpiration**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

簽章到期日（以秒為單位，從1970年1月1日開始起算），格林尼治平均時間 (GMT) ，不包括閏秒。

</dd> <dt>

**SignatureInception**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

簽章變成有效的日期和時間（以秒為單位，從1970年1月1日開始起算），格林尼治平均時間 (GMT) ，不包括閏秒。

</dd> <dt>

**SignerName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

產生 SIG RR 之簽署者的功能變數名稱。

</dd> <dt>

**TypeCovered**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

此 SIG 所涵蓋的 RR 類型。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                              |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 命名空間<br/>                | 根 \\ MicrosoftDNS<br/>                                                          |
| MOF<br/>                      | <dl> <dt>Dnsprov mof</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MicrosoftDNS SIGType 類別的 CreateInstanceFromPropertyData 方法 \_**](microsoftdns-sigtype-createinstancefrompropertydata.md)
</dt> <dt>

[**Modify MicrosoftDNS \_ SIGType 類別的方法**](microsoftdns-sigtype-modify.md)
</dt> <dt>

[**MicrosoftDNS \_ ResourceRecord**](microsoftdns-resourcerecord.md)
</dt> </dl>

 

 





