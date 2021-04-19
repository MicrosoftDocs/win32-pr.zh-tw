---
description: 抓取物件所支援的屬性。
ms.assetid: 842bd4d6-0824-4597-bb5d-9ef8769055fb
title: 'WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED 命令 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: bd816e1dc4ce9c3cbb1fb3c0b118004983baea54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984333"
---
# <a name="wpd_command_object_properties_get_supported-command"></a>WPD \_ 命令 \_ 物件 \_ 屬性 \_ 取得 \_ 支援的命令

**WPD \_ 命令 \_ 物件 \_ 屬性 \_ GET \_ 支援** 的命令會抓取物件所支援的屬性。

## <a name="command-category"></a>命令類別目錄

**WPD \_ 類別 \_ 物件 \_ 屬性**

## <a name="parameters"></a>參數

驅動程式需要下列參數。



| 參數                                         | VarType        | Description                                                            |
|---------------------------------------------------|----------------|------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ 物件 \_ 屬性 \_ 物件 \_ 識別碼** | **VT \_ LPWSTR** | 必要。 包含所要求之屬性的物件識別碼。 |



 

## <a name="return-value"></a>傳回值

驅動程式應該會傳回下列結果。



| 結果                                                | VarType         | Description                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------|-----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ 物件 \_ 屬性 \_ 索引 \_ 鍵** | **VT \_ 不明** | 必要。 [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md)介面，指定所有支援的屬性。                                                                                                                                                                                                            |
| **WPD \_ 屬性 \_ 通用 \_ HRESULT**                    | **VT \_ 錯誤**   | 必要。 表示整體成功或失敗的 **HRESULT** 值。 可能的結果值包括 [Windows 可攜式裝置錯誤碼](error-constants.md)。 如果呼叫端提出不正確要求，驅動程式應該 **\_ 從 WIN32 傳回 HRESULT \_ (\_ 不支援的錯誤 \_)** 但不需要傳回任何其他結果值。 |
| **WPD \_ 屬性 \_ 常見的 \_ 驅動程式 \_ 錯誤碼 \_**        | **VT \_ UI4**     | 選擇性。 驅動程式特定的錯誤碼。 這通常只用于驅動程式測試，或者驅動程式、裝置和用戶端都是一起設計的。                                                                                                                                                                                                |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**命令**](commands.md)
</dt> </dl>

 

 




