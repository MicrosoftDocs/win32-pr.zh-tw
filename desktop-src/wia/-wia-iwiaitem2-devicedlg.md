---
description: 顯示對話方塊，讓使用者準備取得影像。
ms.assetid: 2d7246ec-fb90-4538-b717-b9e3813c1696
title: 'IWiaItem2：:D eviceDlg 方法 (Wia. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3337e74a621b6431b5bbfa429692717def447c82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113313"
---
# <a name="iwiaitem2devicedlg-method"></a>IWiaItem2：:D eviceDlg 方法

顯示對話方塊，讓使用者準備取得影像。

## <a name="syntax"></a>語法


```C++
HRESULT DeviceDlg(
  [in]      LONG      lFlags,
  [in]      HWND      hwndParent,
  [in]      BSTR      bstrFolderName,
  [in]      BSTR      bstrFilename,
  [in]      LONG      *plNumFiles,
  [in, out] BSTR      **ppbstrFilePaths,
  [in, out] IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lFlags* \[在\]
</dt> <dd>

類型： **LONG**

指定一組旗標來控制對話方塊的操作。 值可以是0以代表預設行為，或 \_ \_ [**WiaFlag**](-wia-wiaflag.md)中所述的任何 WIA 裝置對話方塊旗標。

</dd> <dt>

*hwndParent* \[在\]
</dt> <dd>

類型： **HWND**

父視窗的控制碼。

</dd> <dt>

*bstrFolderName* \[在\]
</dt> <dd>

類型： **BSTR**

指定要傳送檔案的資料夾名稱。

</dd> <dt>

*bstrFilename* \[在\]
</dt> <dd>

類型： **BSTR**

指定範本的檔案名。

</dd> <dt>

*plNumFiles* \[在\]
</dt> <dd>

類型： **LONG \** _

_PpbstrFilePaths * 陣列中專案數目的指標。

</dd> <dt>

*ppbstrFilePaths* \[in、out\]
</dt> <dd>

類型： **BSTR \* \***

掃描的檔案之路徑陣列的指標位址。 在 IWiaItem2 之前，初始化指標以指向大小為零的陣列 (0) 0 **：呼叫:D evicedlg** 。

</dd> <dt>

*ppIWiaItem2* \[in、out\]
</dt> <dd>

類型： **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***

[**IWiaItem2**](-wia-iwiaitem2.md)介面指標陣列的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

這個方法會向使用者顯示一個對話方塊，讓應用程式用來收集影像取得所需的所有資訊。 它也可用來指定影像掃描屬性，例如亮度和對比。

在這個方法傳回之後，應用程式可以使用 [**IWiaTransfer**](-wia-iwiatransfer.md) 介面來取得影像。

應用程式必須針對它們透過 *ppIWiaItem2* 參數接收之介面指標陣列中的每個元素，呼叫 [IUnknown：： Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)方法。 應用程式也必須使用 [CoTaskMemFree](/windows/win32/api/combaseapi/nf-combaseapi-cotaskmemfree)釋放陣列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Wia</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia .idl</dt> </dl> |



 

 
