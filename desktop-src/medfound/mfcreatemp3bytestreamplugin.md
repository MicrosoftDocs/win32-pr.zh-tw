---
description: 建立 MP3 媒體來源的位元組資料流程處理常式。
ms.assetid: A213BAEF-D98F-485B-8840-BE131E9B26C0
title: MFCreateMP3ByteStreamPlugin 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MFCreateMP3ByteStreamPlugin
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0b8bcd153471ddd8acd648d5775b4dc964693a56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974143"
---
# <a name="mfcreatemp3bytestreamplugin-function"></a>MFCreateMP3ByteStreamPlugin 函式

\[此 API 不受支援，而且可能會在未來變更或無法使用。 相反地，應用程式應該使用 [來源解析](source-resolver.md) 程式來建立 MP3 媒體來源。\]

建立 MP3 媒體來源的位元組資料流程處理常式。

## <a name="syntax"></a>語法


```C++
HRESULT __stdcall MFCreateMP3ByteStreamPlugin(
  _In_  REFIID riid,
  _Out_ LPVOID *ppvHandler
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*riid* \[在\]
</dt> <dd>

所要求介面的介面識別項 (IID)。 將此參數設定為 **IID \_ IMFByteStreamHandler** ，以接收 [**IMFByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler) 介面的指標。

</dd> <dt>

*ppvHandler* \[擴展\]
</dt> <dd>

接收介面的指標。 呼叫端必須釋放介面。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

此函數沒有相關聯的匯入程式庫。 若要呼叫這個函式，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 mf.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows Vista<br/>                             |
| 伺服器支援結束<br/>    | Windows Server 2008<br/>                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎函式](media-foundation-functions.md)
</dt> <dt>

[配置處理常式和 Byte-Stream 處理常式](scheme-handlers-and-byte-stream-handlers.md)
</dt> <dt>

[來源解析程式](source-resolver.md)
</dt> </dl>

 

 
