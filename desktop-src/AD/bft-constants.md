---
title: 'BFT 常數 (Ntdsbcli) '
description: BFT 常數會當做位旗標使用，以識別 Active Directory Domain Services 備份中的不同檔案類型。
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9607b5e61e5689d8895b39a11aa7e813fc7fcbe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934220"
---
# <a name="bft-constants"></a>BFT 常數

BFT 常數會當做位旗標使用，以識別 Active Directory Domain Services 備份中的不同檔案類型。

<dl> <dt>

<span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**BFT \_ 記錄檔 \_ 目錄**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>



檔案屬於記錄檔目錄。


</dt> </dl> </dd> <dt>

<span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**BFT \_ 資料庫 \_ 目錄**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>



檔案屬於資料庫目錄。


</dt> </dl> </dd> <dt>

<span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**BFT \_ 目錄**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



指定的路徑是目錄，而不是檔案名。


</dt> </dl> </dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>**BFT \_ 記錄檔**
</dt> <dd> <dl> <dt>

0x21
</dt> <dt>



指定隸屬于記錄檔目錄中的記錄檔。


</dt> </dl> </dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT \_ 記錄檔 \_ 目錄**
</dt> <dd> <dl> <dt>

0x22
</dt> <dt>



檔案是記錄檔目錄的路徑。


</dt> </dl> </dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**BFT \_ 檢查點 \_ 目錄**
</dt> <dd> <dl> <dt>

0x23
</dt> <dt>



檔案是檢查點目錄的路徑。


</dt> </dl> </dd> <dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ 資料庫**
</dt> <dd> <dl> <dt>

0x44
</dt> <dt>



檔案是屬於資料庫目錄的目錄服務資料庫。


</dt> </dl> </dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**BFT \_ 修補 \_ 檔案**
</dt> <dd> <dl> <dt>

0x25
</dt> <dt>



檔案是屬於記錄檔目錄的修補檔案。


</dt> </dl> </dd> <dt>

<span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT \_ 不明**
</dt> <dd> <dl> <dt>

0x0F
</dt> <dt>



無法辨識該檔案。 檔案不會與已知的檔案名和檔案類型一致。


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Ntdsbcli。h</dt> </dl> |



 

 





