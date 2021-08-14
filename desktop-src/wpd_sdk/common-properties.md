---
description: Windows可攜式裝置 (WPD) 支援下列命令參數的屬性。
ms.assetid: 03eff101-5c36-48ea-9dcd-2c4ee29a2ac6
title: '命令參數 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Command
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: e5c58652c27d62e2954e86b9170e2f0a2d4ae4021743ced769adbf46a1f082b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118431055"
---
# <a name="command-parameters"></a>命令參數

Windows可攜式裝置 (WPD) 支援下列命令參數的屬性。




| **屬性**                                            | **VarType**     | **說明**                                                                                                                                                              |
|---------------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ 通用 \_ 用戶端 \_ 資訊**          | **VT \_ 不明** | 驅動程式用來識別用戶端的 [**IPortableDeviceValues**](iportabledevicevalues.md) 介面。                                                             |
| **WPD \_ 屬性 \_ 通用 \_ 用戶端 \_ 資訊 \_ 內容** | **VT \_ LPWSTR**  | 驅動程式指定的內容，用來識別所有後續作業的用戶端。                                                                                          |
| **WPD \_ 屬性 \_ 通用 \_ 命令 \_ 類別目錄**            | **VT \_ CLSID**   | 命令之 **PROPERTYKEY** 值的 **GUID** 部分。                                                                                                            |
| **WPD \_ 屬性 \_ 通用 \_ 命令 \_ 識別碼**                  | **VT \_ UI4**     |  (PID 的持續性唯一識別碼) 部分的命令 **PROPERTYKEY** 值。                                                                                          |
| **WPD \_ 屬性 \_ 通用 \_ 命令 \_ 目標**              | **VT \_ LPWSTR**  | 目標物件識別碼。                                                                                                                                                |
| **WPD \_ 屬性 \_ 常見的 \_ 驅動程式 \_ 錯誤碼 \_**          | **VT \_ UI4**     | WPD 驅動程式所傳回的驅動程式特定錯誤碼。                                                                                                                       |
| **WPD \_ 屬性 \_ 通用 \_ HRESULT**                      | **VT \_ 錯誤**   | 特定作業的 WPD 驅動程式所傳回的 **HRESULT** 值。                                                                                                   |
| **WPD \_ 屬性 \_ 通用 \_ 物件 \_ 識別碼**                  | **VT \_ 不明** | Variant 型別 **VT \_ LPWSTR** 的 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)介面，其中包含物件識別碼的清單。 |
| **WPD \_ 屬性 \_ 常見的 \_ 持續性 \_ 唯一 \_ 識別碼**      | **VT \_ 不明** | Variant 型別 **VT \_ LPWSTR** 的 [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md)介面，其中包含 pid 的清單。               |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**屬性和屬性**](properties-and-attributes.md)
</dt> </dl>

 

 




