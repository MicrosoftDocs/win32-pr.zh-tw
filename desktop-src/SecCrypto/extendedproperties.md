---
description: 代表 ExtendedProperty 物件的集合。
ms.assetid: 9de25994-9f0b-47a0-b4c8-781aec782f88
title: ExtendedProperties 物件
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExtendedProperties
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 0225582217df56f486a44f12e3ca6ea0003130fdb209fb67e9f9e4ee258764d2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007236"
---
# <a name="extendedproperties-object"></a>ExtendedProperties 物件

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista 和 Windows XP。 相反地，請使用 (PInvoke) 的平台叫用服務來呼叫 WIN32 API 函式 [**CertGetCertificateCoNtextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty) 並取得屬性。 如需 PInvoke 的詳細資訊，請參閱 [平台叫用教學](https://msdn.microsoft.com/library/aa288468.aspx)課程。 [.Net 和 cryptoapi Via p/invoke：第1部分](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic5)和[.net，以及透過 p/invoke](/previous-versions/ms867087(v=msdn.10)#netcryptoapi_topic6)叫用的 cryptoapi：[利用 CAPICOM 和 p/invoke 擴充 .net 密碼](/previous-versions/ms867087(v=msdn.10))編譯的第二部分，可能也很有用。\]

**ExtendedProperties** 物件代表 [**ExtendedProperty**](extendedproperty.md)物件的集合。 每個物件都代表單一的擴充屬性。

## <a name="when-to-use"></a>使用時機

**ExtendedProperties** 物件是用來執行下列工作：

-   從集合中加入或移除 [**ExtendedProperty**](extendedproperty.md) 物件。
-   取得集合中的擴充屬性數目。
-   從集合中取出特定的 [**ExtendedProperty**](extendedproperty.md) 物件。
-   逐一查看集合。

## <a name="members"></a>成員

**ExtendedProperties** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#extendedproperties-object)

### <a name="methods"></a>方法

**ExtendedProperties** 物件有這些方法。



| 方法                                      | 描述                                                                                    |
|:--------------------------------------------|:-----------------------------------------------------------------------------------------------|
| [**添加**](extendedproperties-add.md)       | 將 [**ExtendedProperty**](extendedproperty.md) 物件加入至集合。<br/>      |
| [**移除**](extendedproperties-remove.md) | 從集合中移除 [**ExtendedProperty**](extendedproperty.md) 物件。<br/> |



 

### <a name="properties"></a>屬性

**ExtendedProperties** 物件具有這些屬性。



| 屬性                                                   | 存取類型          | 描述                                                                                                                                                                                                                     |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](extendedproperties-newenum.md)<br/> | 唯讀<br/> | 在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 這個屬性會在 Visual Basic 腳本版本 (VBScript) 中隱藏。<br/> |
| [**計數**](extendedproperties-count.md)<br/>       | 唯讀<br/> | 抓取集合中的 [**ExtendedProperty**](extendedproperty.md) 物件數目。<br/>                                                                                                                      |
| [**項目**](extendedproperties-item.md)<br/>         | 唯讀<br/> | 抓取 [**ExtendedProperty**](extendedproperty.md) 物件，該物件代表集合的索引延伸屬性。 這是預設屬性。<br/>                                                      |



 

## <a name="remarks"></a>備註

無法建立 **ExtendedProperties** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
