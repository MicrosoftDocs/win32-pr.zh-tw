---
description: 代表 (CPS) 指標或使用者注意事項辨識符號的認證實務聲明。
ms.assetid: 857af3d6-aa7b-429a-a056-72573232f72c
title: 限定詞物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifier
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3b1740e064cac53f93d9c81603477a1230c7fd7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983056"
---
# <a name="qualifier-object"></a>限定詞物件

\[**限定詞** 物件可在 [需求] 區段中指定的作業系統中使用。 相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]

辨識 **符號** 物件代表 (CPS) 指標或使用者注意事項辨識符號的認證實務聲明。

## <a name="when-to-use"></a>使用時機

辨識 **符號** 物件是用來執行下列工作：

-   取出辨識符號的物件識別碼。
-   抓取 (URI) 的統一資源識別項，指向 [*憑證授權單位*](../secgloss/c-gly.md) 單位 (CA) 發佈的 CPS。
-   取出與辨識符號相關聯的組織名稱。
-   取出使用者通知的名稱和內容。

## <a name="members"></a>成員

**限定詞** 物件有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**限定詞** 物件具有這些屬性。



| 屬性                                                          | 存取類型          | Description                                                                                                                         |
|:------------------------------------------------------------------|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| [**CPSPointer**](qualifier-cpspointer.md)<br/>             | 唯讀<br/> | 抓取包含指向 CA 所發佈之 CPS 之 URI 的字串。<br/>                                       |
| [**ExplicitText**](qualifier-explicittext.md)<br/>         | 唯讀<br/> | 抓取包含使用者通知內容的字串。 這個屬性可以是空的。<br/>                             |
| [**NoticeNumbers**](qualifier-noticenumbers.md)<br/>       | 唯讀<br/> | 抓取包含使用者聲明編號集合的 **NoticeNumbers** 物件。 這個屬性可以是空的。<br/>    |
| [**老**](qualifier-oid.md)<br/>                           | 唯讀<br/> | 抓取識別辨識符號的 [**OID**](oid.md) 物件。 這是預設屬性。<br/>                      |
| [**OrganizationName**](qualifier-organizationname.md)<br/> | 唯讀<br/> | 抓取字串，其中包含與辨識符號相關聯的組織名稱。 這個屬性可以是空的。<br/> |



 

## <a name="remarks"></a>備註

無法建立 **限定詞** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
