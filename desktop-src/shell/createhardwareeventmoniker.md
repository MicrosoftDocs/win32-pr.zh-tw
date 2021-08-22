---
description: 建立代表硬體元件及其相關事件處理常式的標記。 自動播放會使用此函式來允許應用程式使用自動播放事件。
title: CreateHardwareEventMoniker 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: 42f2da51bac93733a74113d3a567802975aca18be2a34f6fa349ff65349749c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118460552"
---
# <a name="createhardwareeventmoniker-function"></a>CreateHardwareEventMoniker 函式

\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。 它可能會在 Windows 的後續版本中變更或無法使用。\]

建立代表硬體元件及其相關事件處理常式的標記。 自動播放會使用此函式來允許應用程式使用自動播放事件。

## <a name="syntax"></a>語法


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*clsid* \[在\]
</dt> <dd>

類型： **REFCLSID**

標記所系結之類別的識別碼。

</dd> <dt>

*pszEventHandler* \[在\]
</dt> <dd>

類型： **LPCTSTR**

事件處理常式的名稱。

</dd> <dt>

*ppmoniker* \[擴展\]
</dt> <dd>

類型： **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***

接收 [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) 介面指標之指標變數的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

註冊正在執行的應用程式時，請使用 **CreateHardwareEventMoniker** ，讓這些應用程式能夠存取自動播放事件。 若要在執行中的應用程式中使用自動播放事件，您必須先建立新的元件來執行 [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) 介面。 使用 **處理常式** 索引鍵下特定處理常式專案的 InitCmdLine 值來初始化這個介面，因為自動播放不會呼叫 [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) 方法。

您應該呼叫 **CreateHardwareEventMoniker** 來取得代表您的元件和其事件處理常式的標記。 然後，使用 *ppmoniker* 參數中所傳回的值，在執行中的物件資料表中註冊您的元件 (衰減) 如範例所示。

請注意， **CreateHardwareEventMoniker** 並未定義在標頭檔中。 若要在程式碼中使用它，您必須透過呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)來取得 Shsvcs.dll 檔案的控制碼。 然後，您可以在對 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 的呼叫中使用該控制碼，以取得 **CreateHardwareEventMoniker** 函式的實例。

呼叫 [**IRunningObjectTable：： Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) 需要您在登錄中輸入下列 **AppID** 資訊。

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>None</dt> </dl>       |
| DLL<br/>                      | <dl> <dt>Shsvcs.dll</dt> </dl> |



 

 
