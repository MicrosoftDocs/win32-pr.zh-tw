---
title: 'IWMDRMLicenseManagement AcquireLicense 方法 (Wmdrmsdk .h) '
description: AcquireLicense 方法會以非同步方式從指定的 URL 取得授權。
ms.assetid: 2e134f39-1f45-4d3a-b7c7-460aa0a250d0
keywords:
- AcquireLicense 方法 windows Media 格式
- AcquireLicense 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，AcquireLicense 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.AcquireLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ad8251650c8a7e16c6eb2fc957df5e70459239c0cd6cf1184b5209ae51b6aaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701124"
---
# <a name="iwmdrmlicensemanagementacquirelicense-method"></a>IWMDRMLicenseManagement：： AcquireLicense 方法

**AcquireLicense** 方法會以非同步方式從指定的 URL 取得授權。

## <a name="syntax"></a>語法


```C++
HRESULT AcquireLicense(
  [in]  BSTR     bstrURL,
  [in]  BSTR     bstrHeaderData,
  [in]  BSTR     bstrActions,
  [in]  DWORD    dwFlags,
  [out] IUnknown **ppunkCancelationCookie
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bstrURL* \[在\]
</dt> <dd>

取得授權之授權伺服器的 URL。 傳遞 **Null** 可讓方法剖析內容標頭中的 URL。

</dd> <dt>

*bstrHeaderData* \[在\]
</dt> <dd>

要傳遞至授權伺服器的內容標頭。 如果 *bstrURL* 為 **Null**，方法將會剖析此標頭中的 URL。 如果 *dwFlags* 設定為 [WMDRM \_ 取得 \_ 授權 \_ 舊版 \_ NONSILENT]，請將此值設定為金鑰識別碼，而不是整個內容標頭。

</dd> <dt>

*bstrActions* \[在\]
</dt> <dd>

字串，包含要在授權中要求許可權的零或多個動作。 字串的格式必須如下：

-   每個動作都必須定義于 ACTION 元素內。 元素的資料是動作字串。
-   所有動作元素都必須包含在時元素內。

    例如，要求授權來播放內容的字串格式如下：

    ```C++
    <ACTIONLIST><ACTION></ACTION></ACTIONLIST>
    ```

    

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

授權取得選項旗標。 設定為下表中的其中一個常數。



| 常數                                   | 描述                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| WMDRM \_ 取得 \_ 授權 \_ 無訊息            | 系統會直接透過網際網路發出授權，而不會向用戶端應用程式進行任何確認。              |
| WMDRM \_ 取得 \_ 授權 \_ NONSILENT         | DRM 子系統會建立授權要求，並以非同步方式傳回以張貼至授權伺服器。 |
| WMDRM \_ 取得 \_ 授權 \_ 舊版 \_ NONSILENT | 與 WMDRM \_ 取得 \_ 授權 NONSILENT 相同 \_ ，不同之處在于將會建立 DRM 版本1授權挑戰。           |



 

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

這個方法會以非同步方式執行。 它會在呼叫後立即傳回，然後在處理完成時產生 **MEWMDRMLicenseAcquisitionCompleted** 事件。 針對非無訊息授權取得作業，藉由呼叫 **IMFMediaEvent：： GetValue** 取得的事件值是 **IUnknown** 指標。 您可以呼叫所抓取 **IUnknown** 介面的 **QueryInterface** 方法，以取得 [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md)介面的實例。

如需使用 Windows 媒體 DRM 用戶端擴充 api 的非同步方法的詳細資訊，請參閱[使用媒體基礎事件模型](using-the-media-foundation-model.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-----------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wmdrmsdk。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>Wmdrmsdk .lib</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDRMLicenseManagement 介面**](iwmdrmlicensemanagement.md)
</dt> <dt>

[**無訊息授權取得**](silent-license-acquisition.md)
</dt> </dl>

 

 





