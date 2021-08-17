---
title: NetworkSettings 物件
description: 針對腳本，提供工作排程器服務用來取得網路設定檔的設定。
ms.assetid: 86ac26c3-c868-4886-8f0b-3a6f6efe3e9d
keywords:
- NetworkSettings 物件工作排程器
- NetworkSettings 物件工作排程器，說明
topic_type:
- apiref
api_name:
- NetworkSettings
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddc5e247ad3de50268c6075f8956687f92800c4e901788b5098a0cef868bb202
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117759690"
---
# <a name="networksettings-object"></a>NetworkSettings 物件

針對腳本，提供工作排程器服務用來取得網路設定檔的設定。

## <a name="members"></a>成員

**NetworkSettings** 物件具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**NetworkSettings** 物件具有這些屬性。



| 屬性                                        | 存取類型           | 描述                                                                                    |
|:------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------|
| [**Id**](networksettings-id.md)<br/>     | 讀取/寫入<br/> | 取得或設定可識別網路設定檔的 GUID 值。<br/>                        |
| [**名稱**](networksettings-name.md)<br/> | 讀取/寫入<br/> | 取得或設定網路設定檔的名稱。 此名稱會用於顯示用途。 <br/> |



 

## <a name="remarks"></a>備註

針對工作讀取或撰寫您自己的 XML 時，會使用工作排程器架構的 [**NetworkSettings**](taskschedulerschema-networksettings-settingstype-element.md) 元素來指定網路設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 類型程式庫<br/>             | <dl> <dt>Taskschd.msc .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Taskschd.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[工作排程器物件](task-scheduler-objects.md)
</dt> <dt>

[工作排程器](task-scheduler-start-page.md)
</dt> </dl>

 

 





