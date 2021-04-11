---
description: SetPort 函式會設定與印表機埠相關聯的狀態。
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: 'SetPort 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab986128c9561b7b95de668367cafb0b3e6cd636
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026700"
---
# <a name="setport-function"></a><span data-ttu-id="d3c95-103">SetPort 函式</span><span class="sxs-lookup"><span data-stu-id="d3c95-103">SetPort function</span></span>

<span data-ttu-id="d3c95-104">**SetPort** 函式會設定與印表機埠相關聯的狀態。</span><span class="sxs-lookup"><span data-stu-id="d3c95-104">The **SetPort** function sets the status associated with a printer port.</span></span>

## <a name="syntax"></a><span data-ttu-id="d3c95-105">語法</span><span class="sxs-lookup"><span data-stu-id="d3c95-105">Syntax</span></span>


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d3c95-106">參數</span><span class="sxs-lookup"><span data-stu-id="d3c95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3c95-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3c95-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c95-108">以零結尾的字串指標，指定埠所連接之印表機伺服器的名稱。</span><span class="sxs-lookup"><span data-stu-id="d3c95-108">Pointer to a zero-terminated string that specifies the name of the printer server to which the port is connected.</span></span> <span data-ttu-id="d3c95-109">如果埠是在本機電腦上，請將此參數設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="d3c95-109">Set this parameter to **NULL** if the port is on the local machine.</span></span>

</dd> <dt>

<span data-ttu-id="d3c95-110">*pPortName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3c95-110">*pPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c95-111">指定印表機埠名稱之以零結尾的字串指標。</span><span class="sxs-lookup"><span data-stu-id="d3c95-111">Pointer to a zero-terminated string that specifies the name of the printer port.</span></span>

</dd> <dt>

<span data-ttu-id="d3c95-112">*dwLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3c95-112">*dwLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c95-113">指定 *pPortInfo* 參數所指向的結構類型。</span><span class="sxs-lookup"><span data-stu-id="d3c95-113">Specifies the type of structure pointed to by the *pPortInfo* parameter.</span></span>

<span data-ttu-id="d3c95-114">此值必須是3，其對應至 [**埠 \_ 資訊 \_ 3**](port-info-3.md) 資料結構。</span><span class="sxs-lookup"><span data-stu-id="d3c95-114">This value must be 3, which corresponds to a [**PORT\_INFO\_3**](port-info-3.md) data structure.</span></span>

</dd> <dt>

<span data-ttu-id="d3c95-115">*pPortInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3c95-115">*pPortInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3c95-116">[**埠 \_ 資訊 \_ 3**](port-info-3.md)結構的指標，其中包含要設定的埠狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="d3c95-116">Pointer to a [**PORT\_INFO\_3**](port-info-3.md) structure that contains the port status information to set.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3c95-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3c95-117">Return value</span></span>

<span data-ttu-id="d3c95-118">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="d3c95-118">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d3c95-119">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="d3c95-119">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d3c95-120">備註</span><span class="sxs-lookup"><span data-stu-id="d3c95-120">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d3c95-121">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="d3c95-121">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d3c95-122">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="d3c95-122">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d3c95-123">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="d3c95-123">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d3c95-124">**SetPort** 函數的呼叫者必須以系統管理員身分執行。</span><span class="sxs-lookup"><span data-stu-id="d3c95-124">The caller of the **SetPort** function must be executing as an Administrator.</span></span> <span data-ttu-id="d3c95-125">此外，如果呼叫端是埠監視器或語言監視器，它必須在呼叫 **SetPort** 之前呼叫 [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself)來停止模擬。</span><span class="sxs-lookup"><span data-stu-id="d3c95-125">Additionally, if the caller is a Port Monitor or Language Monitor, it must call [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself) to cease impersonation before it calls **SetPort**.</span></span>

<span data-ttu-id="d3c95-126">呼叫 **SetPort** 的所有程式都必須擁有伺服器存取權， \_ \_ 才能存取埠所連接的伺服器。</span><span class="sxs-lookup"><span data-stu-id="d3c95-126">All programs that call **SetPort** must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="d3c95-127">當您設定 [印表機埠狀態值] 的 [嚴重性值埠 \_ 狀態 \_ 類型] \_ 錯誤時，列印多工緩衝處理器會停止將作業傳送至埠。</span><span class="sxs-lookup"><span data-stu-id="d3c95-127">When you set a printer port status value with the severity value PORT\_STATUS\_TYPE\_ERROR, the print spooler stops sending jobs to the port.</span></span> <span data-ttu-id="d3c95-128">當其他 **SetPort** 呼叫清除埠狀態時，列印多工緩衝處理器會繼續將作業傳送至埠。</span><span class="sxs-lookup"><span data-stu-id="d3c95-128">The print spooler resumes sending jobs to the port when the port status is cleared by another call to **SetPort**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3c95-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3c95-129">Requirements</span></span>



| <span data-ttu-id="d3c95-130">需求</span><span class="sxs-lookup"><span data-stu-id="d3c95-130">Requirement</span></span> | <span data-ttu-id="d3c95-131">值</span><span class="sxs-lookup"><span data-stu-id="d3c95-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3c95-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3c95-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d3c95-133">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3c95-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d3c95-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3c95-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d3c95-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3c95-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d3c95-136">標頭</span><span class="sxs-lookup"><span data-stu-id="d3c95-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3c95-137"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="d3c95-137"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d3c95-138">程式庫</span><span class="sxs-lookup"><span data-stu-id="d3c95-138">Library</span></span><br/>                  | <dl> <span data-ttu-id="d3c95-139"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d3c95-139"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d3c95-140">DLL</span><span class="sxs-lookup"><span data-stu-id="d3c95-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3c95-141"><dt>Winspool.drv. winspool.drv</dt></span><span class="sxs-lookup"><span data-stu-id="d3c95-141"><dt>Winspool.drv</dt></span></span> </dl>                   |
| <span data-ttu-id="d3c95-142">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d3c95-142">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d3c95-143">**SetPortW** (Unicode) 和 **SetPortA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="d3c95-143">**SetPortW** (Unicode) and **SetPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="d3c95-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3c95-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3c95-145">列印</span><span class="sxs-lookup"><span data-stu-id="d3c95-145">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d3c95-146">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="d3c95-146">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d3c95-147">**埠 \_ 資訊 \_ 3**</span><span class="sxs-lookup"><span data-stu-id="d3c95-147">**PORT\_INFO\_3**</span></span>](port-info-3.md)
</dt> </dl>

 

