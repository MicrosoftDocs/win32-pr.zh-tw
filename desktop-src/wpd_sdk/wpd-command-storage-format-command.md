---
description: WPD \_ 命令 \_ 儲存格式命令會將 \_ 裝置上的儲存體功能物件格式化。
ms.assetid: 5dc06ed3-791f-4c6b-9fb3-42452e948e0d
title: 'WPD_COMMAND_STORAGE_FORMAT 命令 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_STORAGE_FORMAT
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 763323a8c2a66319ab84636a5d7b2d46a6edb37d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981313"
---
# <a name="wpd_command_storage_format-command"></a>WPD \_ 命令 \_ 儲存 \_ 格式命令

**WPD \_ 命令 \_ 儲存 \_ 格式** 命令會將裝置上的儲存體功能物件格式化。

## <a name="command-category"></a>命令類別目錄

**WPD \_ 類別 \_ 儲存體**

## <a name="parameters"></a>參數

驅動程式需要下列參數。



| 參數                          | VarType    | Description                                              |
|------------------------------------|------------|----------------------------------------------------------|
| WPD \_ 屬性 \_ 儲存體 \_ 物件 \_ 識別碼 | VT \_ LPWSTR | 必要。 要格式化之儲存媒體的物件識別碼。 |



 

## <a name="return-value"></a>傳回值

驅動程式應該會傳回下列結果。



| 結果                                         | VarType   | Description                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ 通用 \_ HRESULT**             | VT \_ 錯誤 | 必要。 **HRESULT** ，表示執行命令的成功或失敗。 如果呼叫端提出不正確要求，驅動程式應該會傳回 **\_ \_ \_ 不 \_ 支援的 WIN32 (錯誤)** ，而且不需要傳回任何其他的結果值。 錯誤碼包括 [Windows 可攜式裝置錯誤代碼](error-constants.md) 或任何其他適當的錯誤碼。 |
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

 

 




