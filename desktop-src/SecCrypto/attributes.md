---
description: 表示屬性物件的集合。
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Attributes 物件
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61936fff0421c43a07483fb8489cca755154a8cfbdd524da5837b12f90add969
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773179"
---
# <a name="attributes-object"></a>Attributes 物件

\[CAPICOM 是僅限32位的元件，可供下列作業系統使用： Windows Server 2008、Windows Vista Windows XP。 請改用 [**system.string 命名空間中的**](/dotnet/api/system.security.cryptography?view=dotnet-plat-ext-3.1&preserve-view=true) [**CryptographicAttributeObjectCollection 類別**](/dotnet/api/system.security.cryptography.cryptographicattributeobjectcollection?view=dotnet-plat-ext-3.1&preserve-view=true)。\]

**Attributes** 物件表示 [**屬性**](attribute.md)物件的集合。 每個 [**屬性**](attribute.md) 物件都代表訊息的單一屬性。

## <a name="when-to-use"></a>使用時機

**Attributes** 物件用來執行下列工作：

-   新增或移除集合中的特定 [**屬性**](attribute.md) 物件。
-   清除集合。
-   取得集合中的屬性數目。
-   從集合中取出特定 [**屬性**](attribute.md) 物件。
-   逐一查看集合。

## <a name="members"></a>成員

**Attributes** 物件具有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**Attributes** 物件有這些方法。



| 方法                              | 描述                                                                       |
|:------------------------------------|:----------------------------------------------------------------------------------|
| [**添加**](attributes-add.md)       | 將 [**屬性**](attribute.md) 物件加入至集合。<br/>       |
| [**清除**](attributes-clear.md)   | 清除集合中的所有 [**屬性**](attribute.md) 物件。<br/> |
| [**移除**](attributes-remove.md) | 從集合中移除 [**屬性**](attribute.md) 物件。<br/>  |



 

### <a name="properties"></a>屬性

**Attributes** 物件具有這些屬性。



| 屬性                                           | 存取類型          | 描述                                                                                                                                                                                                                     |
|:---------------------------------------------------|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_NewEnum**](attributes-newenum.md)<br/> | 唯讀<br/> | 在可以用來列舉集合的物件上，抓取 [**IEnumVARIANT**](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。 這個屬性會在 Visual Basic 腳本版本 (VBScript) 中隱藏。<br/> |
| [**計數**](attributes-count.md)<br/>       | 唯讀<br/> | 抓取集合中的 [**屬性**](attribute.md) 物件數目。<br/>                                                                                                                                    |
| [**項目**](attributes-item.md)<br/>         | 唯讀<br/> | 抓取代表索引屬性的 [**屬性**](attribute.md) 物件。 這是預設屬性。<br/>                                                                                             |



 

## <a name="remarks"></a>備註

無法建立 **屬性** 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows Vista<br/>                                                               |
| 伺服器支援結束<br/> | Windows Server 2008<br/>                                                         |
| 可轉散發套件<br/>       | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[加密物件](cryptography-objects.md)
</dt> </dl>

 

 
