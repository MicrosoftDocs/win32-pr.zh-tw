---
description: WPD \_ 命令 \_ sms SEND 命令會透過 \_ sms 功能物件，起始傳送短訊息服務 (sms) 訊息。
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: 'WPD_COMMAND_SMS_SEND 命令 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2378ae2b17102fc2bbee568b7f5baa82da554bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982956"
---
# <a name="wpd_command_sms_send-command"></a>WPD \_ 命令 \_ SMS \_ SEND 命令

**WPD \_ 命令 \_ sms \_ SEND** 命令會透過 sms 功能物件，起始傳送短訊息服務 (sms) 訊息。

## <a name="command-category"></a>命令類別目錄

**WPD \_ 類別 \_ SMS**

## <a name="parameters"></a>參數

驅動程式需要下列參數。



| 參數                              | VarType             | Description                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WPD \_ 屬性 \_ 通用 \_ 命令 \_ 目標 | VT \_ LPWSTR          | 必要。 應傳送訊息之 SMS 功能物件的物件識別碼。 不同的 SMS 功能物件可以有不同的設定。                                                                                     |
| WPD \_ 屬性 \_ SMS \_ 收件者          | VT \_ LPWSTR          | 必要。 收件者的 URI。                                                                                                                                                                                                  |
| WPD \_ 屬性 \_ SMS \_ 訊息 \_ 類型      | VT \_ UI4             | 必要。 指出訊息類型 (文字或二進位) 的 [**SMS \_ 訊息 \_ 類型**](sms-message-types.md) 列舉值。                                                                                                        |
| WPD \_ 屬性 \_ SMS \_ 文字 \_ 訊息      | VT \_ LPWSTR          | 選擇性。 如果 **WPD \_ 屬性 \_ SMS \_ 訊息 \_ 類型** 指出文字訊息，這就是訊息字串; 否則，就不會包含此參數。                                                                                  |
| WPD \_ 屬性 \_ SMS \_ 二進位 \_ 訊息    | VT \_ 向量 \| vt \_ UI1 | 選擇性。 如果 **WPD \_ 屬性 \_ SMS \_ 訊息 \_ 類型** 指出二進位訊息，這就是位元組陣列的指標; 否則不會包含此參數。 值的第一個 DWORD 是陣列的長度（以位元組為單位）。 |



 

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

 

 




