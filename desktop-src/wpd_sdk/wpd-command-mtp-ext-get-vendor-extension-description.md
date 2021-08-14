---
description: WPD \_ 命令 \_ MTP \_ EXT \_ 的取得 \_ 廠商 \_ 擴充 \_ 功能 description 命令會抓取廠商延伸的描述字串。 這個字串是由 DeviceInfo 資料集所定義。
ms.assetid: 3741fc97-bbe6-41f0-9c0f-fb2f22225fa3
title: 'WPD_COMMAND_MTP_EXT_GET_VENDOR_EXTENSION_DESCRIPTION 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31622676161065ec685640789bc51eef64165542a9ebe4c9367ea1a03195e7cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118193505"
---
# <a name="wpd_command_mtp_ext_get_vendor_extension_description-command"></a>WPD \_ 命令 \_ MTP \_ EXT \_ GET \_ 廠商 \_ EXTENSION \_ DESCRIPTION 命令

**WPD \_ 命令 \_ MTP EXT 的 \_ \_ 取得 \_ 廠商 \_ 擴充功能 \_ description** 命令會抓取廠商延伸的描述字串。 這個字串是由 **DeviceInfo** 資料集所定義。

## <a name="command-category"></a>命令類別目錄

**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**

## <a name="parameters"></a>參數

此命令沒有任何參數。

## <a name="return-value"></a>傳回值

驅動程式會傳回下列結果。



| 結果                                                      | VarType    | Description                                                  |
|-------------------------------------------------------------|------------|--------------------------------------------------------------|
| **WPD \_ 屬性 \_ MTP \_ EXT \_ * \_ 延伸模組 \_ 描述** | VT \_ LPWSTR | 必要。 指定廠商延伸的描述字串。 |



 

## <a name="calling-methods"></a>呼叫方法

只能使用 [**IPortableDevice：： SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand)直接呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-----------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>WpdMtpExtensions。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[支援 MTP 擴充功能](supporting-mtp-extensions.md)
</dt> </dl>

 

 




