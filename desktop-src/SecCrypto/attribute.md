---
description: 表示單一驗證的屬性。
ms.assetid: 71c4543b-683f-4ffa-8301-c40c46c490b3
title: Attribute 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 34c0800874dc9380b8c9034df2867fc3d1fb578d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984755"
---
# <a name="attribute-object"></a>Attribute 物件

\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。 請改用 [**system.string 命名空間中的**](/previous-versions/windows/) [**CryptographicAttributeObject 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true)。\]

**Attribute** 物件代表單一已驗證的屬性。

## <a name="when-to-use"></a>使用時機

**屬性** 物件是用來執行下列工作：

-   設定或取出屬性的 CAPICOM 名稱。
-   設定或取得屬性的值，例如簽署時間、簽署的檔案名稱，或檔的描述。

## <a name="members"></a>成員

**Attribute** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Attribute** 物件具有這些屬性。



| 屬性                                    | 存取類型           | Description                                                                                   |
|:--------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------|
| [**Name**](attribute-name.md)<br/>   | 讀取/寫入<br/> | 設定或抓取屬性的 CAPICOM 名稱。 這是預設屬性。<br/> |
| [**值**](attribute-value.md)<br/> | 讀取/寫入<br/> | 設定或抓取屬性的值。<br/>                                      |



 

## <a name="remarks"></a>備註

您可以建立 **屬性** 物件，而且可以安全地進行腳本處理。 **屬性** 物件的 PROGID 為 CAPICOM。屬性。1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**加密物件**](cryptography-objects.md)
</dt> </dl>

 

 
