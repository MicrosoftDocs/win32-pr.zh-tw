---
description: WPD \_ 命令 \_ 儲存體 \_ 退出命令會彈出可由電腦從遠端彈出的儲存媒體。
ms.assetid: 38d4dd56-e898-4890-8328-eb2b03cdbd12
title: 'WPD_COMMAND_STORAGE_EJECT 命令 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_EJECT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2a35b376ed9688217edfde03c76aed962d3e5fb74dc3d8bb7cc927ef1f621c9b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119839008"
---
# <a name="wpd_command_storage_eject-command"></a>WPD \_ 命令 \_ 儲存體 \_ 退出命令

**WPD \_ 命令 \_ 儲存體 \_ 退出** 命令會彈出可由電腦從遠端彈出的儲存媒體。

## <a name="command-category"></a>命令類別目錄

**WPD \_ 類別 \_ 儲存體**

## <a name="parameters"></a>參數

驅動程式需要下列參數。



| 參數                          | VarType    | 描述                                             |
|------------------------------------|------------|---------------------------------------------------------|
| WPD \_ 屬性 \_ 儲存體 \_ 物件 \_ 識別碼 | VT \_ LPWSTR | 必要。 要退出之儲存物件的物件識別碼。 |



 

## <a name="return-value"></a>傳回值

驅動程式應該會傳回下列結果。



| 結果                                         | VarType   | 描述                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ 通用 \_ HRESULT**             | VT \_ 錯誤 | 必要。 **HRESULT** ，表示執行命令的成功或失敗。 如果呼叫端提出不正確要求，驅動程式應該會傳回 **\_ \_ \_ 不 \_ 支援的 WIN32 (錯誤)** ，而且不需要傳回任何其他的結果值。 錯誤碼包含[Windows 可攜式裝置的錯誤碼](error-constants.md)或任何其他適當的錯誤碼。 |
| **WPD \_ 屬性 \_ 常見的 \_ 驅動程式 \_ 錯誤碼 \_** | VT \_ UI4   | 選擇性。 驅動程式特定的錯誤碼。 這通常只會用於驅動程式測試，或者驅動程式、裝置和用戶端都是一起設計的。                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>呼叫方法

只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**命令**](commands.md)
</dt> </dl>

 

 




