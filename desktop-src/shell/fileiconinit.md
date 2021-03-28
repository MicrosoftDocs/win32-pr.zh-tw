---
description: 初始化或重新初始化系統映射清單。
ms.assetid: 4e661326-157e-4c75-86df-cd213e01c3e5
title: FileIconInit 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIconInit
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 090f35cc576caf6f99a8d5822a0304f15383e8db
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104319143"
---
# <a name="fileiconinit-function"></a><span data-ttu-id="d32ac-103">FileIconInit 函式</span><span class="sxs-lookup"><span data-stu-id="d32ac-103">FileIconInit function</span></span>

<span data-ttu-id="d32ac-104">初始化或重新初始化系統映射清單。</span><span class="sxs-lookup"><span data-stu-id="d32ac-104">Initializes or reinitializes the system image list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d32ac-105">語法</span><span class="sxs-lookup"><span data-stu-id="d32ac-105">Syntax</span></span>


```C++
BOOL FileIconInit(
  _In_ BOOL fRestoreCache
);
```



## <a name="parameters"></a><span data-ttu-id="d32ac-106">參數</span><span class="sxs-lookup"><span data-stu-id="d32ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d32ac-107">*fRestoreCache* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d32ac-107">*fRestoreCache* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d32ac-108">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="d32ac-108">Type: **BOOL**</span></span>

<span data-ttu-id="d32ac-109">**TRUE** 表示從磁片還原系統映射快取;否則 **為 FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d32ac-109">**TRUE** to restore the system image cache from disk; **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d32ac-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d32ac-110">Return value</span></span>

<span data-ttu-id="d32ac-111">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="d32ac-111">Type: **BOOL**</span></span>

<span data-ttu-id="d32ac-112">如果已成功重新整理快取，**則為 TRUE** ，如果初始化失敗，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d32ac-112">**TRUE** if the cache was successfully refreshed, **FALSE** if the initialization failed.</span></span>

## <a name="remarks"></a><span data-ttu-id="d32ac-113">備註</span><span class="sxs-lookup"><span data-stu-id="d32ac-113">Remarks</span></span>

<span data-ttu-id="d32ac-114">如果您在自己的進程中使用系統映射清單，您必須在下列時間呼叫 **FileIconInit** ：</span><span class="sxs-lookup"><span data-stu-id="d32ac-114">If you are using system image lists in your own process, you must call **FileIconInit** at the following times:</span></span>

-   <span data-ttu-id="d32ac-115">啟動時。</span><span class="sxs-lookup"><span data-stu-id="d32ac-115">On launch.</span></span>
-   <span data-ttu-id="d32ac-116">在設定 [**SPI \_ SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa)旗標時回應 [**WM \_ SETTINGCHANGE**](../winmsg/wm-settingchange.md)訊息。</span><span class="sxs-lookup"><span data-stu-id="d32ac-116">In response to a [**WM\_SETTINGCHANGE**](../winmsg/wm-settingchange.md) message when the [**SPI\_SETNONCLIENTMETRICS**](/windows/win32/api/winuser/nf-winuser-systemparametersinfoa) flag is set.</span></span>

<span data-ttu-id="d32ac-117">**FileIconInit** 不包含在標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="d32ac-117">**FileIconInit** is not included in a header file.</span></span> <span data-ttu-id="d32ac-118">您必須直接從 Shell32.dll 使用序數660來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="d32ac-118">You must call it directly from Shell32.dll, using ordinal 660.</span></span>

## <a name="requirements"></a><span data-ttu-id="d32ac-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="d32ac-119">Requirements</span></span>



| <span data-ttu-id="d32ac-120">需求</span><span class="sxs-lookup"><span data-stu-id="d32ac-120">Requirement</span></span> | <span data-ttu-id="d32ac-121">值</span><span class="sxs-lookup"><span data-stu-id="d32ac-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d32ac-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d32ac-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d32ac-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d32ac-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="d32ac-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d32ac-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d32ac-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d32ac-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="d32ac-126">DLL</span><span class="sxs-lookup"><span data-stu-id="d32ac-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d32ac-127"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d32ac-127"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
