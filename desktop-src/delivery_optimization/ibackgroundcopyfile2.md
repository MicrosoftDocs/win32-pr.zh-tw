---
title: 'IBackgroundCopyFile2 介面 (>deliveryoptimization .h) '
description: 使用 IBackgroundCopyFile2 介面指定檔案的新遠端名稱，並取出要下載的範圍清單。
ms.assetid: 28233310-9F2A-4567-B0B1-B549F862F3C8
keywords:
- IBackgroundCopyFile2 介面
- IBackgroundCopyFile2 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4a866c8f18ee1dfb57f32ac3b2b9999e10106522
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025008"
---
# <a name="ibackgroundcopyfile2-interface"></a>IBackgroundCopyFile2 介面

使用 **IBackgroundCopyFile2** 介面指定檔案的新遠端名稱，並取出要下載的範圍清單。

**IBackgroundCopyFile2** 介面繼承自 [**IBackgroundCopyFile**](ibackgroundcopyfile.md)介面。

若要取得 **IBackgroundCopyFile2** 介面指標，請針對介面識別碼使用 __Uuidof (IBackgroundCopyFile2) 來呼叫 **IBackgroundCopyFile：： QueryInterface** 方法。 使用 **IBackgroundCopyFile2** 介面指標來呼叫 [**IBackgroundCopyFile**](ibackgroundcopyfile.md) 和 **IBackgroundCopyFile2** 方法。

## <a name="members"></a>成員

**IBackgroundCopyFile2** 介面繼承自 [**IBackgroundCopyFile**](ibackgroundcopyfile.md)。 **IBackgroundCopyFile2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IBackgroundCopyFile2** 介面具有這些方法。



| 方法                                                             | 描述                                                                      |
|:-------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**GetFileRanges**](ibackgroundcopyfile2-getfileranges-method.md) | 抓取您要從 URL 下載的範圍陣列。<br/> |
| [**SetRemoteName**](ibackgroundcopyfile2-setremotename-method.md) | 將遠端名稱變更為新的 URL。<br/>                                 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 定義為83E81B93-0873-474D-8A8C-F2018B1A939C<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyFile**](ibackgroundcopyfile.md)
</dt> </dl>

 

 





