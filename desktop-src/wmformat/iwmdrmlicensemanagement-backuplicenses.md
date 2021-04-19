---
title: 'IWMDRMLicenseManagement BackupLicenses 方法 (Wmdrmsdk .h) '
description: BackupLicenses 方法會在本機授權存放區中建立授權的備份。
ms.assetid: f265254d-b240-4a9f-9c67-de9c92e8a14d
keywords:
- BackupLicenses 方法 windows Media 格式
- BackupLicenses 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，BackupLicenses 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.BackupLicenses
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61c7f676b532353c839a428571f6d28540851bee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987087"
---
# <a name="iwmdrmlicensemanagementbackuplicenses-method"></a>IWMDRMLicenseManagement：： BackupLicenses 方法

**BackupLicenses** 方法會在本機授權存放區中建立授權的備份。

## <a name="syntax"></a>語法


```C++
HRESULT BackupLicenses(
  [in]  BSTR     bstrBackupDirectory,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrBackupDirectory* \[在\]
</dt> <dd>

將備份授權之目標位置的 UNC 路徑。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

旗標，指定要使用的備份選項。 目前唯一支援的旗標是 WMDRM \_ 備份 \_ 覆寫，它會設定方法以覆寫目錄中任何現有的備份檔案。

</dd> <dt>

*ppunkCancelationCookie* \[擴展\]
</dt> <dd>

指標，接收識別此非同步呼叫之物件的 **IUnknown** 介面指標。 這個介面指標可透過呼叫 [**IWMDRMEventGenerator：： CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) 方法，用來取消非同步呼叫。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                          | Description                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl> | 此方法已成功。<br/> |



 

## <a name="remarks"></a>備註

這個方法會以非同步方式執行。 它會在呼叫後立即傳回，然後在處理完成時產生一連串的 **MEWMDRMLicenseBackupProgress** 事件，後面接著 **MEWMDRMLicenseBackupCompleted** 事件。 藉由呼叫 **IMFMediaEvent：： GetValue** 取得的每個 **MEWMDRMLicenseBackupProgress** 事件的值都是 **IUnknown** 指標。 您可以呼叫所抓取 **IUnknown** 介面的 **QueryInterface** 方法，以取得 [**IWMDRMLicenseBackupRestoreStatus**](iwmdrmlicensebackuprestorestatus.md)介面的實例。

如需使用 Windows Media DRM 用戶端擴充 Api 的非同步方法的詳細資訊，請參閱 [使用媒體基礎事件模型](using-the-media-foundation-model.md)。

並非所有授權都可進行備份。 這個方法只會備份允許的授權。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicenseManagement 介面**](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





