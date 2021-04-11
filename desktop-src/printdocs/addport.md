---
description: AddPort 函式會將埠的名稱新增至支援的埠清單。 AddPort 函數是由埠監視器匯出。
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: 'AddPort 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: 00e589b59b15c898887090b12348f23fac57fda3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852228"
---
# <a name="addport-function"></a><span data-ttu-id="4e2bf-104">AddPort 函式</span><span class="sxs-lookup"><span data-stu-id="4e2bf-104">AddPort function</span></span>

<span data-ttu-id="4e2bf-105">**AddPort** 函式會將埠的名稱新增至支援的埠清單。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-105">The **AddPort** function adds the name of a port to the list of supported ports.</span></span> <span data-ttu-id="4e2bf-106">**AddPort** 函數是由埠監視器匯出。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-106">The **AddPort** function is exported by the port monitor.</span></span>

## <a name="syntax"></a><span data-ttu-id="4e2bf-107">語法</span><span class="sxs-lookup"><span data-stu-id="4e2bf-107">Syntax</span></span>


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a><span data-ttu-id="4e2bf-108">參數</span><span class="sxs-lookup"><span data-stu-id="4e2bf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4e2bf-109">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e2bf-109">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e2bf-110">以零結束的字串指標，指定埠所連接的伺服器名稱。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-110">A pointer to a zero-terminated string that specifies the name of the server to which the port is connected.</span></span> <span data-ttu-id="4e2bf-111">如果此參數為 **Null**，則埠為本機。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-111">If this parameter is **NULL**, the port is local.</span></span>

</dd> <dt>

<span data-ttu-id="4e2bf-112">*hWnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e2bf-112">*hWnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e2bf-113">**AddPort** 對話方塊父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-113">A handle to the parent window of the **AddPort** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4e2bf-114">*pMonitorName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4e2bf-114">*pMonitorName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4e2bf-115">以零結束的字串指標，指定與埠相關聯的監視器。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-115">A pointer to a zero-terminated string that specifies the monitor associated with the port.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4e2bf-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="4e2bf-116">Return value</span></span>

<span data-ttu-id="4e2bf-117">如果函式成功，則傳回值為非零值。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-117">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="4e2bf-118">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-118">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="4e2bf-119">備註</span><span class="sxs-lookup"><span data-stu-id="4e2bf-119">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="4e2bf-120">這是封鎖或同步函式，可能不會立即傳回。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-120">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="4e2bf-121">此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-121">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="4e2bf-122">從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-122">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="4e2bf-123">**AddPort** 函式會流覽網路以尋找現有的埠，並顯示使用者的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-123">The **AddPort** function browses the network to find existing ports, and displays a dialog box for the user.</span></span> <span data-ttu-id="4e2bf-124">**AddPort** 函式應藉由呼叫 [**EnumPorts**](enumports.md)來驗證使用者輸入的埠名稱，以確保沒有重複的名稱存在。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-124">The **AddPort** function should validate the port name entered by the user by calling [**EnumPorts**](enumports.md) to ensure that no duplicate names exist.</span></span>

<span data-ttu-id="4e2bf-125">**AddPort** 函式的呼叫端必須具有伺服器 \_ 存取權 \_ ，才能存取埠所連接的伺服器。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-125">The caller of the **AddPort** function must have SERVER\_ACCESS\_ADMINISTER access to the server to which the port is connected.</span></span>

<span data-ttu-id="4e2bf-126">若要在不顯示對話方塊的情況下新增埠，請呼叫 **XcvData** 函式，而不是 **AddPort**。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-126">To add a port without displaying a dialog box, call the **XcvData** function instead of **AddPort**.</span></span> <span data-ttu-id="4e2bf-127">如需有關 **XcvData** 的詳細資訊，請參閱 Microsoft Windows 驅動程式開發工具組 (DDK) 。</span><span class="sxs-lookup"><span data-stu-id="4e2bf-127">For more information about **XcvData**, see the Microsoft Windows Driver Development Kit (DDK).</span></span>

## <a name="requirements"></a><span data-ttu-id="4e2bf-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="4e2bf-128">Requirements</span></span>



| <span data-ttu-id="4e2bf-129">需求</span><span class="sxs-lookup"><span data-stu-id="4e2bf-129">Requirement</span></span> | <span data-ttu-id="4e2bf-130">值</span><span class="sxs-lookup"><span data-stu-id="4e2bf-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4e2bf-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4e2bf-131">Minimum supported client</span></span><br/> | <span data-ttu-id="4e2bf-132">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e2bf-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4e2bf-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4e2bf-133">Minimum supported server</span></span><br/> | <span data-ttu-id="4e2bf-134">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4e2bf-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4e2bf-135">標頭</span><span class="sxs-lookup"><span data-stu-id="4e2bf-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="4e2bf-136"><dt>Winspool.drv (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="4e2bf-136"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="4e2bf-137">程式庫</span><span class="sxs-lookup"><span data-stu-id="4e2bf-137">Library</span></span><br/>                  | <dl> <span data-ttu-id="4e2bf-138"><dt>Winspool.drv .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4e2bf-138"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="4e2bf-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4e2bf-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4e2bf-140"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4e2bf-140"><dt>Spoolss.dll</dt></span></span> </dl>                    |
| <span data-ttu-id="4e2bf-141">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="4e2bf-141">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="4e2bf-142">**AddPortW** (Unicode) 和 **AddPortA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="4e2bf-142">**AddPortW** (Unicode) and **AddPortA** (ANSI)</span></span><br/>                                                 |



## <a name="see-also"></a><span data-ttu-id="4e2bf-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4e2bf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4e2bf-144">列印</span><span class="sxs-lookup"><span data-stu-id="4e2bf-144">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="4e2bf-145">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="4e2bf-145">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="4e2bf-146">**DeletePort**</span><span class="sxs-lookup"><span data-stu-id="4e2bf-146">**DeletePort**</span></span>](deleteport.md)
</dt> <dt>

[<span data-ttu-id="4e2bf-147">**EnumPorts**</span><span class="sxs-lookup"><span data-stu-id="4e2bf-147">**EnumPorts**</span></span>](enumports.md)
</dt> <dt>

[<span data-ttu-id="4e2bf-148">**SetPort**</span><span class="sxs-lookup"><span data-stu-id="4e2bf-148">**SetPort**</span></span>](setport.md)
</dt> </dl>

 

 




