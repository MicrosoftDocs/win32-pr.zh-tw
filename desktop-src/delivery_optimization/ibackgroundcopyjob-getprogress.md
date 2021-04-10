---
title: 'IBackgroundCopyJob GetProgress 方法 (>deliveryoptimization .h) '
description: 抓取作業相關的進度資訊，例如已傳送的位元組和檔案數目。
ms.assetid: E23C82E1-3805-4C5D-9F18-0DA17F7C473E
keywords:
- GetProgress 方法
- GetProgress 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetProgress 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetProgress
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d49a040bb5656ae6ef6d926a45b31808623e399b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103955"
---
# <a name="ibackgroundcopyjobgetprogress-method"></a>IBackgroundCopyJob：： GetProgress 方法

抓取作業相關的進度資訊，例如已傳送的位元組和檔案數目。

## <a name="syntax"></a>語法


```C++
HRESULT GetProgress(
  [out] BG_JOB_PROGRESS *pProgress
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pProgress* \[擴展\]
</dt> <dd>

包含可用來計算已完成作業之百分比的資料。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                              | Description                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | 成功取回進度資訊。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> </dl>

 

 





