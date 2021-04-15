---
title: 'IResultType 介面 (WdsSharedIDL .h) '
description: 公開屬性類型資訊。
ms.assetid: 68abd470-2505-4836-a17f-f1c14157f8e7
keywords:
- IResultType 介面舊版 Windows 環境功能
- IResultType 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IResultType
api_location:
- WdsSharedIDL.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88451739a6ca2eb600838ea137ebc1ddba98f3a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464916"
---
# <a name="iresulttype-interface"></a>IResultType 介面

> [!NOTE]
> Windows Desktop Search 2.x 是一種淘汰的技術，最初是以 Windows XP 和 Windows Server 2003 的增益集形式提供。 在更新版本中，請改用 [WINDOWS SEARCH API](../search/-search-reference-entry-page.md) 。 

公開屬性類型資訊。

## <a name="members"></a>成員

**IResultType** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IResultType** 也有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**IResultType** 介面具有這些屬性。



| 屬性                                                                 | 存取類型           | Description                                                                           |
|:-------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------|
| [**DisplayName**](-search-2x-iresulttype-displayname.md)<br/>     | 唯讀<br/>  | 類型的當地語系化顯示名稱：<br/>                                        |
| [**GetProperty**](-search-2x-iresulttype-getproperty.md)<br/>     | 讀取/寫入<br/> | 此屬性包含指定的屬性資訊。 <br/>                    |
| [**PreceivedType**](-search-2x-iresulttype-preceivedtype.md)<br/> | 唯讀<br/>  | 這個屬性包含用來識別索引中之類型的字串。 <br/> |
| [**PropertyCount**](-search-2x-iresulttype-propertycount.md)<br/> | 唯讀<br/>  | 這個屬性包含型別所公開的屬性數目。 <br/>      |
| [**UID**](-search-2x-iresulttype-uid.md)<br/>                     | 唯讀<br/>  | 此屬性包含類型的唯一識別碼。 <br/>                |



 

## <a name="remarks"></a>備註

這些方法會公開傳回的資訊類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 與 SP1 \[ desktop 應用程式\]<br/>                             |
| 可轉散發套件<br/>          | Windows 桌面搜尋 (WDS) 3。0<br/>                                               |
| 標頭<br/>                   | <dl> <dt>WdsSharedIDL。h</dt> </dl> |



 

