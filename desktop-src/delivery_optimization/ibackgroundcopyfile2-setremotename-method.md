---
title: 'IBackgroundCopyFile2 SetRemoteName 方法 (>deliveryoptimization .h) '
description: 在下載作業中，將遠端名稱變更為新的 URL。
ms.assetid: 344D4193-C96E-4B94-AA53-F9307FEB2565
keywords:
- SetRemoteName 方法
- SetRemoteName 方法，IBackgroundCopyFile2 介面
- IBackgroundCopyFile2 介面，SetRemoteName 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile2.SetRemoteName
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4afb5448144867c799bd401bc2d7c180d3958f2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465073"
---
# <a name="ibackgroundcopyfile2setremotename-method"></a>IBackgroundCopyFile2：： SetRemoteName 方法

在下載作業中，將遠端名稱變更為新的 URL。

## <a name="syntax"></a>語法


```C++
HRESULT SetRemoteName(
  [in] LPCWSTR RemoteName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RemoteName* \[在\]
</dt> <dd>

以 Null 終止的字串，其中包含伺服器上的檔案名。 如需指定遠端名稱的詳細資訊，請參閱 **RemoteName** 成員。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列傳回值以及其他值。



| 傳回碼                                                                                  | Description                                                                                                           |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>     | Success<br/>                                                                                                    |
| <dl> <dt>**E_INVALIDARG**</dt> </dl> | 新的遠端名稱是不正確 URL，或新的 URL 太長 (URL) 不能超過2200個字元。<br/> |



 

## <a name="remarks"></a>備註

一般來說，如果您想要變更用來傳送檔案的 URL，或想要變更檔案名或路徑，則可以呼叫這個方法。

當這個方法傳回時，不會序列化。 若要將變更序列化，請 [**暫停**](ibackgroundcopyjob-suspend.md) 作業、呼叫這個方法 (如果變更作業中的多個檔案，請使用迴圈) ，然後 [**繼續**](ibackgroundcopyjob-resume.md) 工作。 呼叫 **IBackgroundCopyJob：： Resume** 方法會序列化變更。

如果新遠端名稱的時間戳記或檔案大小與先前的遠端名稱不同，或新伺服器不支援 HTTP 遠端名稱) 的檢查點繼續 (，請重新開機下載。 否則，就會從新伺服器上的相同位置繼續轉移。 請勿重新開機已傳送的檔案。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile2 定義為83e81b93-0873-474d-8a8c-f2018b1a939c<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyFile2**](ibackgroundcopyfile2.md)
</dt> </dl>

 

 





