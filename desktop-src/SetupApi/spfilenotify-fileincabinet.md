---
description: 針對封 \_ 包中找到的每個檔案，SetupIterateCabinet 會將 SPFILENOTIFY FILEINCABINET 通知傳送至回呼常式。 回呼常式必須傳回值，指出是否要解壓縮檔案。
ms.assetid: c6d89759-c0d4-4741-b992-43eaa0dc4f01
title: 'SPFILENOTIFY_FILEINCABINET 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 496db3cef814f2bf366f4cb6f91132efe01a2406
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000331"
---
# <a name="spfilenotify_fileincabinet-message"></a>SPFILENOTIFY \_ FILEINCABINET 訊息

針對封包中找到的每個檔案， [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)會將 **SPFILENOTIFY \_ FILEINCABINET** 通知傳送至回呼常式。 回呼常式必須傳回值，指出是否要解壓縮檔案。


```C++
SPFILENOTIFY_FILEINCABINET
  Param1 = (UINT) FileInCabinetInfo;
  Param2 = (UINT) CabinetFile;
            
```



## <a name="parameters"></a>參數

<dl> <dt>

*Param1* 
</dt> <dd>

封 [**\_ \_ 包 \_ 資訊結構中檔案**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a) 的指標，其中包含封包中檔案的相關資訊。

</dd> <dt>

*Param2* 
</dt> <dd>

以 null 結束的字串指標，其中包含封包檔的檔案名。

</dd> </dl>

## <a name="return-value"></a>傳回值

您的回呼常式應該會傳回下列其中一項。



| 傳回碼                                                                                 | Description                                  |
|---------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**FILEOP \_ SKIP**</dt> </dl> | 不要解壓縮檔案，請略過。<br/> |
| <dl> <dt>**FILEOP \_ DOIT R**</dt> </dl> | 將檔案解壓縮。<br/>                 |



 

如果您的回呼常式 \_ 傳回 FILEOP doit r，則要用於解壓縮檔案的名稱應該在封 [**\_ \_ 包 \_ 資訊**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)結構中傳遞至 *Param1* 的常式之檔案的 **FullTargetName** 成員中指定。

> [!Note]  
> 沒有預設的封包回呼常式。 安裝應用程式應該提供回呼常式來處理 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)所傳送的通知。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Setupapi.log。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[概觀](overview.md)
</dt> <dt>

[通知](notifications.md)
</dt> <dt>

[**封 \_ 包資訊中的 \_ 檔案 \_**](/windows/desktop/api/Setupapi/ns-setupapi-file_in_cabinet_info_a)
</dt> <dt>

[**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)
</dt> </dl>

 

 




