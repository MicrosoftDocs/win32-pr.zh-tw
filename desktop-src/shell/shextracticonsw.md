---
description: 建立從指定檔案解壓縮之圖示的控制碼陣列。
title: SHExtractIconsW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SHExtractIconsW
- SHExtractIconsW
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: 9f138b4e-6a84-4c7e-9521-5f8ffe0eaebf
ms.openlocfilehash: 699b6d5473d97548a22e220372b9f53633cb2346
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109840909"
---
# <a name="shextracticonsw-function"></a>SHExtractIconsW 函式

\[**SHExtractIconsW** 可透過 Windows XP Service Pack 2 (SP2) 取得。 它可能會在後續版本中變更或無法使用。\]

建立從指定檔案解壓縮之圖示的控制碼陣列。

## <a name="syntax"></a>語法


```C++
UINT SHExtractIconsW(
  _In_  LPCWSTR pszFileName,
  _In_  int     nIconIndex,
  _In_  int     cxIcon,
  _In_  int     cyIcon,
  _Out_ HICON   *phIcon,
  _Out_ UINT    *pIconId,
  _In_  UINT    nIcons,
  _In_  UINT    flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>pszfilename* \[在\]
</dt> <dd>

類型： **LPCWSTR**

要從中解壓縮圖示的檔案名指標。

</dd> <dt>

*nIconIndex* \[在\]
</dt> <dd>

類型： **int**

要從名為 *>pszfilename* 之資源中解壓縮的第一個圖示索引。

</dd> <dt>

*cxIcon* \[在\]
</dt> <dd>

類型： **int**

圖示所需的寬度。 請參閱＜備註＞。

</dd> <dt>

*cyIcon* \[在\]
</dt> <dd>

類型： **int**

所需的圖示高度。 請參閱＜備註＞。

</dd> <dt>

*phIcon* \[擴展\]
</dt> <dd>

類型： **HICON \***

當此函式傳回時，會包含圖示控制碼陣列的指標。

</dd> <dt>

*pIconId* \[擴展\]
</dt> <dd>

類型： **UINT \***

當此函式傳回時，會包含最適合目前顯示裝置之已解壓縮圖示的資源識別碼指標。 如果沒有適用于此格式的識別碼，則會包含0xFFFFFFFF。 如果沒有任何其他原因可以取得任何識別碼，則會傳回零。

</dd> <dt>

*nIcons* \[在\]
</dt> <dd>

類型： **UINT**

要從名為 *>pszfilename* 的資源中解壓縮的圖示數目。 只有當資源是 .exe 或 .dll 檔案時，此參數才有效。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

類型： **UINT**

控制此函數的旗標。 如需可能的值，請參閱 [**LoadImage**](/windows/win32/api/winuser/nf-winuser-loadimagea)函數的 *fuLoad* 參數。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **UINT**

如果成功，則為非零值;否則為零。

## <a name="remarks"></a>備註

**SHExtractIconsW** 會從下列檔案類型中解壓縮。

-   可執行檔 (.exe)
-   DLL ( .dll) 
-    ( .ico) 圖示
-   資料指標 (。當前) 
-    ( 的動畫資料指標) 
-   Bitmap (.bmp)

從 Windows 3 提取。也支援 *x* 16 位可執行檔 ( .exe 或 .dll) 。

*CxIcon* 和 *cyIcon* 參數指定要解壓縮的圖示大小。 您可以藉由在 LOWORD 和 HIWORD 之間分割值，在每個參數中解壓縮兩個大小。 將所需的第一個大小放在參數的 LOWORD 中，並將第二個大小放在 HIWORD 中。 例如， *cxIcon* 和 *cyIcon* 的 [**MAKELONG**](/previous-versions/windows/desktop/legacy/ms632660(v=vs.85)) (24，48) 會解壓縮24和48大小的圖示。

呼叫的進程會藉由呼叫 [**DestroyIcon**](/windows/win32/api/winuser/nf-winuser-destroyicon) 函式，負責終結透過此函式解壓縮的所有圖示。

**SHExtractIconsW** 不會依名稱匯出，也不會在公用標頭檔中宣告。 若要使用它，您必須宣告相符的原型，並使用 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 來要求 Shell32.dll 的函式指標，而這些指標可以用來呼叫這個函數。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (5.0 版或更新版本) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **SHExtractIconsW** (Unicode) <br/>                                                                      |



 

 
