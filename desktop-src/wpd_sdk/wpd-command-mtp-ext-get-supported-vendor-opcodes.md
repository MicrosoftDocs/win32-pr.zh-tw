---
description: WPD \_ 命令 \_ MTP EXT \_ - \_ 取得 \_ 支援的 \_ 廠商 opcode \_ 碼命令傳送 MTP 命令區塊。 沒有與此命令相關聯的後續資料階段。
ms.assetid: 397ae29c-f81c-410e-9670-db69c099a321
title: 'WPD_COMMAND_MTP_EXT_GET_SUPPORTED_VENDOR_OPCODES 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8713c739da98c179ecc2b7bf042905e4fd06ad7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984779"
---
# <a name="wpd_command_mtp_ext_get_supported_vendor_opcodes-command"></a>WPD \_ 命令 \_ MTP \_ EXT \_ GET \_ 支援的 \_ 廠商 opcode \_ 碼命令

**WPD \_ 命令 \_ MTP EXT- \_ \_ 取得 \_ 支援的廠商 opcode \_ \_ 碼** 命令傳送 MTP 命令區塊。 沒有與此命令相關聯的後續資料階段。

## <a name="command-category"></a>命令類別目錄

**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**

## <a name="parameters"></a>參數

此命令沒有任何參數。

## <a name="return-value"></a>傳回值

驅動程式會傳回下列結果。



| 結果                                                | VarType | Description                                                                                              |
|-------------------------------------------------------|---------|----------------------------------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ MTP \_ EXT \_ * \_ 操作 \_ 代碼** | VT \_ UI4 | 必要。 **IPortableDevicePropVariantCollection** ，其中包含所有廠商擴充的作業代碼。 |



 

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

 

 




