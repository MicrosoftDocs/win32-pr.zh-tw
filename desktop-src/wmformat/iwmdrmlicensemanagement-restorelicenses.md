---
title: 'IWMDRMLicenseManagement RestoreLicenses 方法 (Wmdrmsdk .h) '
description: RestoreLicenses 方法會從藉由呼叫 BackupLicenses 方法所建立的授權備份還原授權。
ms.assetid: 83e4b748-0f69-4a9e-b531-047c9a2be1fe
keywords:
- RestoreLicenses 方法 windows Media 格式
- RestoreLicenses 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，RestoreLicenses 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.RestoreLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2a35fdd33df2387bb59dfac64f554dd8b5953fa3015afec6ca643725b9bd58f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117846936"
---
# <a name="iwmdrmlicensemanagementrestorelicenses-method"></a>IWMDRMLicenseManagement：： RestoreLicenses 方法

**RestoreLicenses** 方法會從藉由呼叫 [**BackupLicenses**](iwmdrmlicensemanagement-backuplicenses.md)方法所建立的授權備份還原授權。

## <a name="syntax"></a>語法


```C++
HRESULT RestoreLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrBackupDirectory* \[在\]
</dt> <dd>

將從中還原授權之位置的 UNC 路徑。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

指定要使用之還原選項的旗標。 目前唯一支援的旗標是 WMDRM \_ RESTORE \_ 賦予，可在必要時將方法設定為執行還原的一部分。

</dd> <dt>

*ppunkCancelationCookie* \[擴展\]
</dt> <dd>

指標，接收識別此非同步呼叫之物件的 **IUnknown** 介面指標。 這個介面指標可透過呼叫 [**IWMDRMEventGenerator：： CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) 方法，用來取消非同步呼叫。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | 描述                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

這個方法會以非同步方式執行。 它會在呼叫後立即傳回，然後在處理完成時產生一連串的 **MEWMDRMLicenseRestoreProgress** 事件，後面接著 **MEWMDRMLicenseRestoreCompleted** 事件。 藉由呼叫 **IMFMediaEvent：： GetValue** 取得的每個 **MEWMDRMLicenseRestoreProgress** 事件的值都是 **IUnknown** 指標。 您可以呼叫所抓取 **IUnknown** 介面的 **QueryInterface** 方法，以取得 [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md)介面的實例。

如需使用 Windows 媒體 DRM 用戶端擴充 api 的非同步方法的詳細資訊，請參閱[使用媒體基礎事件模型](using-the-media-foundation-model.md)。

備份可以來自本機電腦或不同的電腦。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicenseManagement 介面**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





