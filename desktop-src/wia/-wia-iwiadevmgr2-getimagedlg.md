---
description: IWiaDevMgr2：： GetImageDlg 方法會顯示一或多個對話方塊，讓使用者從 Windows 影像取得取得影像 (WIA) 2.0 裝置，並將影像寫入指定的檔案。
ms.assetid: 30a63426-150e-44cf-a03e-7b6da14450f7
title: 'IWiaDevMgr2：： GetImageDlg 方法 (Wia .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.GetImageDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0b03356e40f1c708c852917c890e4c1bf96b98cd18ccf82b75ebcaaccaa69597
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814038"
---
# <a name="iwiadevmgr2getimagedlg-method"></a>IWiaDevMgr2：： GetImageDlg 方法

**IWiaDevMgr2：： GetImageDlg** 方法會顯示一或多個對話方塊，讓使用者從 Windows 影像取得取得影像 (WIA) 2.0 裝置，並將影像寫入指定的檔案。 這個方法會擴充 [**IWiaDevMgr2：： SelectDeviceDlg**](-wia-iwiadevmgr2-selectdevicedlg.md) 的功能，以在單一 API 呼叫中封裝取得影像。

## <a name="syntax"></a>語法


```C++
HRESULT GetImageDlg(
  [in]      LONG      lFlags,
  [in]      BSTR      bstrDeviceID,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in]      BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppItem
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

指定對話方塊的行為。 可以設定為下列值：



| 旗標                                 | 意義                                                                                                                                                                     |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                                    | 預設行為。                                                                                                                                                           |
| WIA \_ 裝置 \_ 對話方塊 \_ 使用 \_ 一般 \_ UI | 使用系統 UI，而不是廠商提供的 UI。 如果系統 UI 無法使用，則會使用廠商 UI。 如果沒有可用的 UI，函數會傳回 E \_ >notimpl。 |



 

</dd> <dt>

*bstrDeviceID* \[在\]
</dt> <dd>

類型： **BSTR**

指定要使用的掃描器。

</dd> <dt>

*hwndParent* \[在\]
</dt> <dd>

類型： **HWND**

擁有 [ **取得影像** ] 對話方塊的視窗控制碼。

</dd> <dt>

*bstrFolderName* \[在\]
</dt> <dd>

類型： **BSTR**

指定儲存掃描之檔案的分成資料夾名稱。

</dd> <dt>

*bstrFilename* \[在\]
</dt> <dd>

類型： **BSTR**

指定要寫入影像資料的檔案名。

</dd> <dt>

*plNumFiles* \[在\]
</dt> <dd>

類型： **LONG \***

要掃描的檔數目指標。

</dd> <dt>

*ppbstrFilePaths* \[在\]
</dt> <dd>

類型： **BSTR \* \***

掃描的檔案之路徑陣列的指標位址。 在呼叫 **IWiaDevMgr2：： GetImageDlg** 之前，初始化指標以指向大小為零的陣列 (0) 。 請參閱 **備註**。

</dd> <dt>

*ppItem* \[in、out\]
</dt> <dd>

類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

[**IWiaItem2**](-wia-iwiaitem2.md)影像掃描來源之指標的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果資料傳輸成功， **IWiaDevMgr2：： GetImageDlg** 會 \_ 傳回 s OK， \_ 如果使用者取消對話方塊，則傳回 FALSE，否則會傳回標準 COM 錯誤。

> [!Note]  
> 如果函數傳回 FALSE，則 *ppbstrFilePaths* 參數不一定是空的 \_ 。 如果使用者取消，則會處理已完成掃描的頁面，並在 *ppbstrFilePaths* 中傳回。 即使未使用它們，您也必須釋放陣列。 請參閱 **備註**。

 

## <a name="remarks"></a>備註

如果應用程式傳遞 **Null** 作為 *bstrDeviceID* 參數的值， **IWiaDevMgr2：： GetImageDlg** 會顯示 [ **選取裝置** ] 對話方塊，讓使用者可以選取 WIA 2.0 輸入裝置。

**在 [檔案**] 功能表上使用以 [**掃描器**] 命名的功能表項目，讓您的應用程式可以使用裝置和映射選取專案。

在 *ppbstrFilePaths* 指向的陣列中的每個 BSTR 上呼叫 [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring) \[ \] ，然後在陣列本身呼叫 [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree) ，以釋放相關聯的記憶體。 如果 \_ 傳回 FALSE，請檢查 *plNumFiles* 指向的值是否不是零。 如果此值不是零，則 \[ \] 會在應用程式中釋放 ppbstrFilePaths i 的資源，因為使用者可能會在掃描一或多個頁面之後取消。 在呼叫 **IWiaDevMgr2：： GetImageDlg** 之前，將 *plNumFiles* 初始化為零。 如果 *plNumFiles* 未初始化為零，而且 COM 基礎結構中的失敗導致函式在 \_ 呼叫 **IWiaDevMgr2：： GetImageDlg** 之前傳回 FALSE，則 *plNumFiles* 會有誤導的垃圾值。

對話方塊必須有足夠的許可權可以 *bstrFolderName* ，以便儲存具有唯一檔案名的檔案。 使用存取控制清單來保護資料夾 (ACL) ，因為它包含使用者資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl> |



 

 
