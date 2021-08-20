---
description: WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ 要讀取的資料 \_ \_ 命令會傳送 MTP 命令區塊，後面接著資料階段。  (將資料從裝置傳送至主機。 ) 。
ms.assetid: 7a76a601-c051-4c0c-bfeb-24e9dddcb9e0
title: 'WPD_COMMAND_MTP_EXT_EXECUTE_COMMAND_WITH_DATA_TO_READ 命令 (WpdMtpExtensions .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08b7e5cfcb807978986c88406332e7270d3c21d5c59ae003c5f8a7fb1009d1a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026757"
---
# <a name="wpd_command_mtp_ext_execute_command_with_data_to_read-command"></a>WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ \_ 要讀取的資料 \_ 命令

**WPD \_ 命令 \_ MTP \_ EXT \_ EXECUTE \_ 命令 \_ 與 \_ \_ 要 \_ 讀取的資料** 命令會傳送 MTP 命令區塊，後面接著資料階段。  (將資料從裝置傳送至主機。 ) 

## <a name="command-category"></a>命令類別目錄

**WPD \_ 類別 \_ MTP \_ EXT- \_ 廠商 \_ 作業**

## <a name="parameters"></a>參數

驅動程式需要下列參數。



| 參數                                      | VarType | 描述                                                                                                                   |
|------------------------------------------------|---------|-------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ MTP \_ EXT \_ 操作 \_ 碼**   | VT \_ UI4 | 必要。 識別廠商延伸的 MTP 作業程式碼。                                                                    |
| **WPD \_ 屬性 \_ MTP \_ EXT \_ 操作 \_ 參數** | VT \_ UI4 | 必要。 **IPortableDevicePropVariantCollection**，識別廠商作業程式碼的必要參數。 |



 

## <a name="return-value"></a>傳回值

驅動程式會傳回下列結果。



| 結果                                                       | VarType    | 描述                                                                                                                                                                                                                         |
|--------------------------------------------------------------|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **WPD \_ 屬性 \_ MTP \_ EXT \_ TRANSFER \_ TOTAL \_ DATA \_ SIZE**     | VT \_ UI8    | 必要。 傳回資料大小總計（以位元組為單位），不包括任何來自裝置的額外負荷。 如果裝置報告未知的 datasize (0xFFFFFFFF) ，驅動程式應該重複呼叫 **ReadData** ，直到收到短的區塊為止 |
| **WPD \_ 屬性 \_ MTP \_ EXT 最 \_ 理想的 \_ 傳輸 \_ 緩衝區 \_ 大小** | VT \_ UI4    | 選擇性。 傳回傳輸緩衝區的最佳大小。                                                                                                                                                                          |
| **WPD \_ 屬性 \_ MTP \_ EXT EXT \_ 傳送 \_ 內容**               | VT \_ LPWSTR | 必要。 指定後續資料傳輸的內容識別碼。                                                                                                                                                           |



 

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

 

 




