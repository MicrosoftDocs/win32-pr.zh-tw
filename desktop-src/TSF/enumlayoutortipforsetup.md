---
title: EnumLayoutOrTipForSetup 函式
description: 列舉安裝程式 UI 或 OOBE 的已安裝鍵盤配置和文字服務。
ms.assetid: 3c6fc11c-36a5-4718-b584-b7f98f1b4180
keywords:
- EnumLayoutOrTipForSetup 函式文字服務架構
topic_type:
- apiref
api_name:
- EnumLayoutOrTipForSetup
api_location:
- input.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9c9a65e0d966684329996e4f5d23370592250a0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965076"
---
# <a name="enumlayoutortipforsetup-function"></a>EnumLayoutOrTipForSetup 函式

列舉安裝程式 UI 或 OOBE 的已安裝鍵盤配置和文字服務。

## <a name="syntax"></a>語法


```C++
UINT CALLBACK EnumLayoutOrTipForSetup(
  _In_  LANGID      langid,
  _Out_ LAYOUTORTIP *pLayoutOrTip,
  _In_  UINT        uBufLength,
  _In_  DWORD       dwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*langid* \[在\]
</dt> <dd>

要列舉之專案的語言識別項。

</dd> <dt>

*pLayoutOrTip* \[擴展\]
</dt> <dd>

接收 LAYOUTORTIP 結構陣列的緩衝區指標。 這可以是 **Null** 來取得專案數目。

</dd> <dt>

*uBufLength* \[在\]
</dt> <dd>

*PLayoutOrTip* 所指向的緩衝區長度。 如果 *pLayoutOrTip* 為 Null，則會忽略此 **值**。

</dd> <dt>

*dwFlags* \[在\]
</dt> <dd>

未使用。 這必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 *pLayoutOrTip* 為 **Null**，則為系統中註冊的鍵盤專案數目;否則，會複製到 *pLayoutOrTip* 中的鍵盤專案數目。

## <a name="remarks"></a>備註

沒有可定義此函式的匯入程式庫，因此必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)取得此函式的指標。

> [!Note]  
> 不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會載入錯誤的 DLL，進而危及應用程式的安全性。 請參閱 [動態連結程式庫搜尋順序](/windows/desktop/Dlls/dynamic-link-library-search-order) ，以取得如何使用不同版本的 Microsoft Windows 正確載入 dll 的相關資訊。

 

LAYOUTORTIP 的定義如下：

``` syntax
typedef struct tagLAYOUTORTIP {
    DWORD dwFlags;
#define LOT_DEFAULT    0x0001 // If this is on, this is a default item. 
#define LOT_DISABLED   0x0002 // if this is on, this is not enabled. 
    WCHAR szId[MAX_PATH]; // Id of the keyboard item in the string format. 
    WCHAR szName[MAX_PATH]; // The description of the keyboard item. 
} LAYOUTORTIP;
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Input.dll</dt> </dl> |



 

