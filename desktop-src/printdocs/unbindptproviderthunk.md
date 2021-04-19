---
description: 關閉列印票證提供者的控制碼。
ms.assetid: ce979c89-9f9d-4e89-b142-beed414caa3f
title: UnbindPTProviderThunk 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnbindPTProviderThunk
api_type:
- DllExport
api_location:
- prntvpt.dll
ms.openlocfilehash: dd87f528603624e9957d8c5f3fb12cc857ec4f5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977895"
---
# <a name="unbindptproviderthunk-function"></a><span data-ttu-id="edbc2-103">UnbindPTProviderThunk 函式</span><span class="sxs-lookup"><span data-stu-id="edbc2-103">UnbindPTProviderThunk function</span></span>

<span data-ttu-id="edbc2-104">\[這項功能不受支援，而且可能會在未來的 Windows 版本中停用或刪除。</span><span class="sxs-lookup"><span data-stu-id="edbc2-104">\[This function is not supported and might be disabled or deleted in future versions of Windows.</span></span> <span data-ttu-id="edbc2-105">[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) 會提供對等的功能，因此應該改用。\]</span><span class="sxs-lookup"><span data-stu-id="edbc2-105">[**PTCloseProvider**](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider) provides equivalent functionality and should be used instead.\]</span></span>

<span data-ttu-id="edbc2-106">關閉列印票證提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="edbc2-106">Closes a handle to a print ticket provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="edbc2-107">語法</span><span class="sxs-lookup"><span data-stu-id="edbc2-107">Syntax</span></span>


```C++
HRESULT UnbindPTProviderThunk(
  _In_ HPTPROVIDER hProvider
);
```



## <a name="parameters"></a><span data-ttu-id="edbc2-108">參數</span><span class="sxs-lookup"><span data-stu-id="edbc2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="edbc2-109">*hProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="edbc2-109">*hProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="edbc2-110">開啟的列印票證提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="edbc2-110">A handle to an open print ticket provider.</span></span> <span data-ttu-id="edbc2-111">[**BindPTProviderThunk**](bindptproviderthunk.md)函數會傳回這個控制碼。</span><span class="sxs-lookup"><span data-stu-id="edbc2-111">This handle is returned by the [**BindPTProviderThunk**](bindptproviderthunk.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="edbc2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="edbc2-112">Return value</span></span>

<span data-ttu-id="edbc2-113">如果方法成功，它會傳回 **S \_ OK**，否則會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="edbc2-113">If the method succeeds, it returns **S\_OK**; otherwise, it returns an **HRESULT** error code.</span></span> <span data-ttu-id="edbc2-114">如需 COM 錯誤碼的詳細資訊，請參閱 [錯誤處理](../com/error-handling-in-com.md)。</span><span class="sxs-lookup"><span data-stu-id="edbc2-114">For more information about COM error codes, see [Error Handling](../com/error-handling-in-com.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="edbc2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="edbc2-115">Requirements</span></span>



| <span data-ttu-id="edbc2-116">需求</span><span class="sxs-lookup"><span data-stu-id="edbc2-116">Requirement</span></span> | <span data-ttu-id="edbc2-117">值</span><span class="sxs-lookup"><span data-stu-id="edbc2-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="edbc2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="edbc2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="edbc2-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edbc2-119">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="edbc2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="edbc2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="edbc2-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="edbc2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="edbc2-122">DLL</span><span class="sxs-lookup"><span data-stu-id="edbc2-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="edbc2-123"><dt>Prntvpt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="edbc2-123"><dt>Prntvpt.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="edbc2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="edbc2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="edbc2-125">列印架構</span><span class="sxs-lookup"><span data-stu-id="edbc2-125">Print Schema</span></span>](./printschema.md)
</dt> <dt>

[<span data-ttu-id="edbc2-126">**PTCloseProvider**</span><span class="sxs-lookup"><span data-stu-id="edbc2-126">**PTCloseProvider**</span></span>](/windows/desktop/api/prntvpt/nf-prntvpt-ptcloseprovider)
</dt> <dt>

[<span data-ttu-id="edbc2-127">列印</span><span class="sxs-lookup"><span data-stu-id="edbc2-127">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="edbc2-128">列印多工緩衝處理器 API 函式</span><span class="sxs-lookup"><span data-stu-id="edbc2-128">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> </dl>

 

