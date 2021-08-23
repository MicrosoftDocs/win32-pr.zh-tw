---
description: '\_SetupIterateCabinet 會將 SPFILENOTIFY FILEEXTRACTED 通知傳送至回呼常式，表示檔案已從封包解壓縮，或是解壓縮失敗，並已取消封包處理。'
ms.assetid: 70ffe06c-e72d-4bb8-a13c-e2946ff72fa6
title: 'SPFILENOTIFY_FILEEXTRACTED 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 56b5028dec11cf2317be080fb82b79bf155be007c66abcbee33492aa229d6317
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665108"
---
# <a name="spfilenotify_fileextracted-message"></a>SPFILENOTIFY \_ FILEEXTRACTED 訊息

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)會將 **SPFILENOTIFY \_ FILEEXTRACTED** 通知傳送至回呼常式，表示檔案已從封包解壓縮，或是解壓縮失敗，並已取消封包處理。


```C++
SPFILENOTIFY_FILEEXTRACTED
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)結構的指標，其中包含解壓縮檔案的路徑資訊。 **FILEPATHS** 結構的 **SourceFile** 成員包含封包的完整來源路徑。 **TargetFile** 成員會提供要安裝在系統上之檔案的完整目標路徑。

</dd> <dt>

*Param2* 
</dt> <dd>

未使用的。

</dd> </dl>

## <a name="return-value"></a>傳回值

封包回呼常式應該會傳回下列其中一個值。



| 傳回碼                                                                               | 描述                                                                                                                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**沒有 \_ 錯誤**</dt> </dl>  | 未發生任何錯誤，請繼續處理封包。<br/>                                                                                                                                |
| <dl> <dt>**錯誤 \_ XXX**</dt> </dl> | 發生指定的類型時發生錯誤。 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) 會傳回零。 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 將會傳回指定的錯誤碼。<br/> |



 

> [!Note]  
> 安裝程式 API 未提供預設的封包回呼常式。 您的安裝應用程式應該提供回呼常式來處理 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) 函式所傳送的通知。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Setupapi.log。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[概觀](overview.md)
</dt> <dt>

[通知](notifications.md)
</dt> <dt>

[**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

