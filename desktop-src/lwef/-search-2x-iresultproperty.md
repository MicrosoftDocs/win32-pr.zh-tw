---
title: 'IResultProperty 介面 (WdsSharedIDL .h) '
description: 公開結果屬性。
ms.assetid: 58d8c516-47c6-4cae-b46c-5127baf3054d
keywords:
- IResultProperty 介面舊版 Windows 環境功能
- IResultProperty 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IResultProperty
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 716c0b3998171731dea5f976afc266fe81b2c613
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966129"
---
# <a name="iresultproperty-interface"></a>IResultProperty 介面

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

公開結果屬性。

## <a name="members"></a>成員

**IResultProperty** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IResultProperty** 也有下列類型的成員：

-   [方法](#methods)
-   [屬性](#properties)

### <a name="methods"></a>方法

**IResultProperty** 介面具有這些方法。



| 方法                                                    | 描述                 |
|:----------------------------------------------------------|:----------------------------|
| [**GoBack**](-search-2x-iresultproperty-goback.md)       | 未實作。<br/> |
| [**GoForward**](-search-2x-iresultproperty-goforward.md) | 未實作。<br/> |



 

### <a name="properties"></a>屬性

**IResultProperty** 介面具有這些屬性。



| 屬性                                                                   | 存取類型          | Description                                           |
|:---------------------------------------------------------------------------|:---------------------|:------------------------------------------------------|
| [**資料類型**](-search-2x-iresultproperty-datatype.md)<br/>         | 唯讀<br/> | 屬性資料類型。 <br/>                   |
| [**DisplayName**](-search-2x-iresultproperty-displayname.md)<br/>   | 唯讀<br/> | 屬性的當地語系化顯示名稱。 <br/>   |
| [**DisplayState**](-search-2x-iresultproperty-displaystate.md)<br/> | 唯讀<br/> | 屬性的 Visability。 <br/>               |
| [**提示**](-search-2x-iresultproperty-hint.md)<br/>                 | 唯讀<br/> | 用來協助資料抓取的特殊值。 <br/> |
| [**IndexColumn**](-search-2x-iresultproperty-indexcolumn.md)<br/>   | 唯讀<br/> | 索引中的屬性資料行名稱。 <br/>      |
| [**UID**](-search-2x-iresultproperty-uid.md)<br/>                   | 唯讀<br/> | 屬性的唯一識別碼。 <br/>       |



 

## <a name="remarks"></a>備註

這些專案會傳回屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 3。0<br/>                                               |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

