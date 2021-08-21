---
description: 指定要用於啟用封包資料通訊協定 (PDP) 內容的驗證通訊協定。
ms.assetid: cd3c28d9-8663-4672-94ba-0a53861086cb
title: AuthProtocol (coNtextType) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuthProtocol
api_type:
- Schema
ms.openlocfilehash: 65b944b2966c9b5cac307f6f8efe6af2f42a1ffa5b4f2f400074caa0efe9f84e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975257"
---
# <a name="authprotocol-contexttype-element"></a>AuthProtocol (coNtextType) 元素

**AuthProtocol (coNtextType)** 元素會指定用來啟用封包資料通訊協定 (PDP) 內容的驗證通訊協定。

元素可以具有下列其中一個值。

| 值      | 意義                                                                 |
|------------|-------------------------------------------------------------------------|
| 以上     | 無驗證通訊協定。                                             |
| PAP      | 未加密的密碼驗證。                                    |
| CHAP     | 挑戰交握驗證通訊協定 (CHAP) 。                      |
|  Eap-mschapv2 | 使用 Microsoft s 挑戰交握驗證通訊協定 (CHAP) 2.0 版。 |



 

這個元素是選擇性的，且僅供 GSM 設定檔使用。 如果未指定專案，而且設定檔適用于 GSM 裝置，則行動寬頻服務將使用「 **無**」。

``` syntax
<xs:element name="AuthProtocol">
    <xs:simpleType>
        <xs:restriction
            base="token"
        >
            <xs:enumeration
                value="NONE"
             />
            <xs:enumeration
                value="PAP"
             />
            <xs:enumeration
                value="CHAP"
             />
            <xs:enumeration
                value="MsCHAPv2"
             />
        </xs:restriction>
    </xs:simpleType>
</xs:element>
```

**AuthProtocol** 元素是由 [**coNtextType**](schema-contexttype-complextype.md)複雜型別定義。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 最低支援的伺服器<br/> | 都不支援<br/>                         |



## <a name="see-also"></a>另請參閱

<dl> <dt>

**架構中的元素定義內容**
</dt> <dt>

[**coNtextType**](schema-contexttype-complextype.md)
</dt> <dt>

**架構實例中可能的直屬父元素**
</dt> <dt>

[**MBNProfile) 內容 (**](schema-context-mbnprofile-element.md)
</dt> </dl>

 

 




