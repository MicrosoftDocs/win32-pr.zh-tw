---
description: WPD \_ 命令 \_ 一般 \_ 重設 \_ 裝置命令會重設裝置。 這並不表示重新格式化;這相當於關閉和開啟裝置。
ms.assetid: 7a630cc9-02ea-46be-9645-8a0306606139
title: 'WPD_COMMAND_COMMON_RESET_DEVICE 命令 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_COMMON_RESET_DEVICE
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: b6a492b7017b8ace6c9118c2f08a1761d7785277fb497474d3e9f39aad60ae8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083371"
---
# <a name="wpd_command_common_reset_device-command"></a>WPD \_ 命令 \_ 一般 \_ 重設 \_ 裝置命令

**WPD \_ 命令 \_ 一般 \_ 重設 \_ 裝置** 命令會重設裝置。 這並不表示重新格式化;這相當於關閉和開啟裝置。

## <a name="command-category"></a>命令類別目錄

**WPD \_ 類別 \_ 通用**

## <a name="parameters"></a>參數

此命令沒有任何參數。

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

 

 




