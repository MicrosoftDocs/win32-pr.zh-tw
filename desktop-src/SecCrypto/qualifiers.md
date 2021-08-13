---
description: 表示限定詞的集合。
ms.assetid: 2f51404d-b26e-4153-b206-ab6b413363a1
title: 'Iads 的限定詞物件 (.h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Qualifiers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0f68dbeefefbe675199522dfbc5b1dab81b8a2840fa8b7d5189c72b811fcba7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900954"
---
# <a name="qualifiers-object"></a>限定詞物件

\[**限定詞** 物件可在 [需求] 區段中指定的作業系統中使用。 相反地，請在 [**system.security.cryptography.x509certificates.x509certificate2**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)命名空間中使用 [**X509Extension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509extension?view=netcore-3.1)，方法是呼叫採用 OID 作為參數的函式，然後使用憑證原則的 Oid 來處理憑證原則延伸中屬於原則資訊的限定詞。\]

**限定詞** 物件代表一組限定詞。

## <a name="when-to-use"></a>使用時機

**限定詞** 物件是用來執行下列工作：

-   從集合中取出特定的擴充屬性。
-   取得集合中的擴充屬性數目。
-   逐一查看集合。

## <a name="members"></a>成員

**限定詞** 物件有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**限定詞** 物件具有這些屬性。



| 屬性                                           | 存取類型          | 描述                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](qualifiers-newenum.md)<br/> | 唯讀<br/> | 在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 這個屬性會在 Visual Basic 腳本版本 (VBScript) 中隱藏。<br/> |
| [**計數**](qualifiers-count.md)<br/>       | 唯讀<br/> | 抓取集合中的限定詞數目。<br/>                                                                                                                                                                |
| [**Item**](qualifiers-item.md)<br/>         | 唯讀<br/> | 抓取代表集合之索引限定詞的辨識 [**符號**](qualifier.md) 物件。 這是預設屬性。<br/>                                                                             |



 

## <a name="remarks"></a>備註

無法建立 **限定詞** 物件。

[**PolicyInformation 限定詞**](policyinformation-qualifiers.md)CAPICOM 物件屬性會傳回辨識符號 **物件。**

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| 標頭<br/>          | <dl> <dt>Iads。h</dt> </dl>      |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
