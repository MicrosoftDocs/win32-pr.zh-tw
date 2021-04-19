---
description: 表示擴充物件的集合。
ms.assetid: b0d69df9-12c4-4872-b883-b029c4350502
title: NoticeNumbers 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NoticeNumbers
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 58d954fdeef66d6d0e5eadb3086cb549b59e5669
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979545"
---
# <a name="noticenumbers-object"></a>NoticeNumbers 物件

\[**NoticeNumbers** 物件可用於 [需求] 區段中指定的作業系統。 如需詳細資訊，請參閱 [**限定詞**](qualifier.md)。\]

**NoticeNumbers** 物件代表 [**延伸**](extension.md)物件的集合。 每個 [**擴充**](extension.md) 物件都代表一個使用者聲明編號。

## <a name="when-to-use"></a>使用時機

**NoticeNumbers** 物件是用來執行下列工作：

-   取得集合中的 [**擴充**](extension.md) 物件數目。
-   從集合中取出特定的 [**擴充**](extension.md) 物件。
-   逐一查看集合。

## <a name="members"></a>成員

**NoticeNumbers** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**NoticeNumbers** 物件具有這些屬性。



| 屬性                                              | 存取類型          | Description                                                                                                                                                                                                                     |
|:------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](noticenumbers-newenum.md)<br/> | 唯讀<br/> | 在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 這個屬性會在 Visual Basic Scripting Edition (VBScript) 中隱藏。<br/> |
| [**計數**](noticenumbers-count.md)<br/>       | 唯讀<br/> | 抓取集合中的 [**擴充**](extension.md) 物件數目。<br/>                                                                                                                                    |
| [**項目**](noticenumbers-item.md)<br/>         | 唯讀<br/> | 抓取 [**擴充**](extension.md) 物件，該物件代表集合的索引聲明編號。<br/> 這是預設屬性。<br/>                                                            |



 

## <a name="remarks"></a>備註

無法建立 **NoticeNumbers** 物件。

NoticeNumbers 物件是在 [**NoticeNumbers**](qualifier-noticenumbers.md) 屬性中使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|----------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
