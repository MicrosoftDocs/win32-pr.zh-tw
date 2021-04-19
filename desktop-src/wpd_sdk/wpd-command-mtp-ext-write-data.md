---
description: WPD \_ 命令 \_ mtp \_ ext \_ WRITE \_ DATA 命令會在執行 WPD \_ 命令 \_ mtp \_ ext ext \_ EXECUTE \_ 命令並執行 \_ \_ 資料 \_ \_ 寫入命令之後，將資料傳送至裝置。
ms.assetid: 96e7164c-17e7-427b-a0fd-4bfbb8215295
title: 'WPD_COMMAND_MTP_EXT_WRITE_DATA 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3eab3809e5cf9bcacc04b68eea9f580cdbe45c03
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993565"
---
# <a name="wpd_command_mtp_ext_write_data-command"></a>WPD \_ 命令 \_ MTP \_ EXT \_ WRITE \_ DATA 命令

**WPD \_ 命令 \_ mtp \_ ext \_ WRITE \_ DATA** 命令會在執行 **WPD \_ 命令 \_ mtp \_ ext ext \_ EXECUTE \_ 命令並執行 \_ \_ 資料 \_ \_ 寫入** 命令之後，將資料傳送至裝置。

## <a name="command-category"></a>命令類別目錄

**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**

## <a name="parameters"></a>參數

驅動程式需要下列參數。



| 參數                                                    | VarType             | Description                                                                            |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ MTP \_ EXT EXT \_ 傳送 \_ 內容**               | VT \_ LPWSTR          | 必要。 識別先前對裝置所做的呼叫所傳回的內容。 |
| **WPD \_ 屬性 \_ MTP \_ EXT \_ TRANSFER \_ \_ BYTES \_ TO \_ WRITE** | VT \_ UI4             | 必要。 指定要寫入的位元組數目。                                      |
| **WPD \_ 屬性 \_ MTP \_ EXT \_ 轉送 \_ 資料**                  | VT \_ 向量 \| vt \_ UI1 | 必要。 識別要將裝置資料複製到其中的緩衝區。                  |



 

## <a name="return-value"></a>傳回值

驅動程式會傳回下列結果。



| 結果                                                     | VarType | Description                                                  |
|------------------------------------------------------------|---------|--------------------------------------------------------------|
| **WPD \_ 屬性 \_ MTP \_ EXT \_ EXT \_ \_ BYTES 寫入位元組數 \_** | VT \_ UI4 | 必要。 指定傳送至裝置的位元組數目。 |



 

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

 

 




