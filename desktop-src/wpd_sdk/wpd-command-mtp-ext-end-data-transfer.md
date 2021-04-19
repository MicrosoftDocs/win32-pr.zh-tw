---
description: WPD \_ 命令 \_ MTP \_ EXT \_ END \_ DATA \_ transfer 命令會完成來自裝置的資料傳輸和讀取回應。
ms.assetid: df2da2e6-ed5a-41a1-be30-844c0d6b409b
title: 'WPD_COMMAND_MTP_EXT_END_DATA_TRANSFER 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f13f451c477d5f0003bf34f485407157d527aa7f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001152"
---
# <a name="wpd_command_mtp_ext_end_data_transfer-command"></a>WPD \_ 命令 \_ MTP \_ EXT \_ END \_ DATA \_ TRANSFER 命令

**WPD \_ 命令 \_ MTP \_ EXT \_ END \_ DATA \_ transfer** 命令會完成來自裝置的資料傳輸和讀取回應。 此傳輸是由 [**WPD \_ 命令 \_ mtp \_ ext \_ execute \_ 命令 \_ 與 \_ data \_ to \_ READ**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-read) 命令或 [**WPD \_ 命令 \_ mtp \_ ext \_ execute \_ 命令 \_ 與 \_ data \_ to \_ WRITE**](/windows/desktop/wpd_sdk/wpd-command-mtp-ext-execute-command-with-data-to-write) 命令起始。

## <a name="command-category"></a>命令類別目錄

**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**

## <a name="parameters"></a>參數

驅動程式需要下列參數。



| 參數                                      | VarType    | Description                                                                  |
|------------------------------------------------|------------|------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ MTP \_ EXT EXT \_ 傳送 \_ 內容** | VT \_ LPWSTR | 必要。 識別先前的方法呼叫所傳回的內容。 |



 

## <a name="return-value"></a>傳回值

驅動程式會傳回下列結果。



| 結果                                        | VarType | Description                                                                                                                             |
|-----------------------------------------------|---------|-----------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ MTP \_ EXT \_ 回應 \_ 碼**   | VT \_ UI4 | 必要的。回應碼為廠商作業程式碼。                                                                                |
| **WPD \_ 屬性 \_ MTP \_ EXT \_ \_ 參數** | VT \_ UI4 | 選擇性。 識別任何回應參數的 **IPortableDevicePropVariantCollection** 集合。 此集合可以是空的。 |



 

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

 

