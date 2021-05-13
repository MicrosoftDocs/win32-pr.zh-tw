---
description: 估計在指定檔案上呼叫處理常式時，執行未知程式碼的風險。 此風險是以瞭解處理常式和檔案的程式碼內容為基礎。
title: EstimateFileRiskLevel 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EstimateFileRiskLevel
api_type:
- DllExport
api_location:
- Winshfhc.dll
ms.assetid: 33a5589a-201b-4d94-afbf-5965a39e2748
ms.openlocfilehash: 2def6cb5bc2ed59a98e9e513aba1b5b578cd8681
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841429"
---
# <a name="estimatefilerisklevel-function"></a>EstimateFileRiskLevel 函式

\[這項功能可在 Windows XP Service Pack 2 (SP2) 到 Windows Vista 中使用。 它可能會在後續版本的 Windows 中改變或無法使用。 用戶端應用程式應該改用 [**IAttachmentExecute**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute) 來呈現可透過電子郵件和郵件附件安全地下載和交換檔案的使用者環境。\]

估計在指定檔案上呼叫處理常式時，執行未知程式碼的風險。 此風險是以瞭解處理常式和檔案的程式碼內容為基礎。

## <a name="syntax"></a>語法


```C++
HRESULT EstimateFileRiskLevel(
  _In_  LPCWSTR         pszFilePath,
  _In_  LPCWSTR         pszExt,
  _In_  LPCWSTR         pszHandler,
  _Out_ FILE_RISK_LEVEL *pfrlEstimate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszFilePath* \[在\]
</dt> <dd>

類型： **LPCWSTR**

以 null 結束的字串指標，其中包含針對處理常式所檢查之檔案的路徑。

</dd> <dt>

*pszExt* \[在\]
</dt> <dd>

類型： **LPCWSTR**

以 null 結束的字串指標，其中包含所檢查之檔案的副檔名（不論是否有前置句點）。 例如，「.txt」或「txt」。

</dd> <dt>

*pszHandler* \[在\]
</dt> <dd>

類型： **LPCWSTR**

以 null 結束的字串指標，其中包含檔案處理常式的路徑。

</dd> <dt>

*pfrlEstimate* \[擴展\]
</dt> <dd>

類型：**檔案 \_ 風險 \_ 層 \* 級**

當此函式成功傳回時，會包含下列其中一個值的指標，以指出預估的風險。

<dt>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>

<span id="FRL_NO_OPINION"></span><span id="frl_no_opinion"></span>**FRL \_ (\_** 0) 的意見


</dt> <dd>

找不到檔案格式或未識別處理常式。 沒有足夠的資訊可提供有意義的答案。

</dd> <dt>

<span id="FRL_LOW"></span><span id="frl_low"></span>

<span id="FRL_LOW"></span><span id="frl_low"></span>**FRL \_低** (1) 


</dt> <dd>

檔案的格式已完全瞭解、已知處理常式，而且不會執行任何多餘的程式碼。

</dd> <dt>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>

<span id="FRL_MODERATE"></span><span id="frl_moderate"></span>**FRL \_適中** (2) 


</dt> <dd>

已識別檔案的格式，但無法充分瞭解將其標示為高或低風險。

</dd> <dt>

<span id="FRL_HIGH"></span><span id="frl_high"></span>

<span id="FRL_HIGH"></span><span id="frl_high"></span>**FRL \_高** (3) 


</dt> <dd>

您可以瞭解檔案格式，並已識別出更高的風險因素。

</dd> <dt>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>

<span id="FRL_BLOCK"></span><span id="frl_block"></span>**FRL \_封鎖** (4) 


</dt> <dd>

此處理程式會特別封鎖檔案格式。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果此函式成功，則會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="remarks"></a>備註

此函式未在公用標頭中宣告，或包含在程式庫檔案中。 若要使用它，您必須將它直接從 Winshfhc.dll 由序數101載入。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Winshfhc.dll (5.1 版或更新版本) </dt> </dl> |



 

 




