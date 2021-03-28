---
description: 此函式會啟用或停用 (EUDC) 的使用者自訂字元支援。
ms.assetid: 9e531d8c-6008-4189-ae25-cda707be5e2c
title: EnableEUDC 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EnableEUDC
api_type:
- DllExport
api_location:
- Gdi32.dll
ms.openlocfilehash: 755ce2e0a659593b17487e86e28f5d454e48122c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972688"
---
# <a name="enableeudc-function"></a><span data-ttu-id="9f8d3-103">EnableEUDC 函式</span><span class="sxs-lookup"><span data-stu-id="9f8d3-103">EnableEUDC function</span></span>

<span data-ttu-id="9f8d3-104">此函式會啟用或停用 (EUDC) 的使用者自訂字元支援。</span><span class="sxs-lookup"><span data-stu-id="9f8d3-104">This function enables or disables support for end-user-defined characters (EUDC).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f8d3-105">語法</span><span class="sxs-lookup"><span data-stu-id="9f8d3-105">Syntax</span></span>


```C++
BOOL EnableEUDC(
  _In_ HDC BOOL fEnableEUDC
);
```



## <a name="parameters"></a><span data-ttu-id="9f8d3-106">參數</span><span class="sxs-lookup"><span data-stu-id="9f8d3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f8d3-107">*fEnableEUDC* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9f8d3-107">*fEnableEUDC* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f8d3-108">將設定為 **TRUE** 以啟用 eudc 的布林值，若為 **FALSE** ，則停用 eudc。</span><span class="sxs-lookup"><span data-stu-id="9f8d3-108">Boolean that is set to **TRUE** to enable EUDC, and to **FALSE** to disable EUDC.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f8d3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="9f8d3-109">Return value</span></span>

<span data-ttu-id="9f8d3-110">如果函式成功，則傳回非零的值。</span><span class="sxs-lookup"><span data-stu-id="9f8d3-110">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="9f8d3-111">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="9f8d3-111">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f8d3-112">備註</span><span class="sxs-lookup"><span data-stu-id="9f8d3-112">Remarks</span></span>

<span data-ttu-id="9f8d3-113">如果已停用 EUDC，嘗試顯示 EUDC 字元將會導致遺失或不正確的字元。</span><span class="sxs-lookup"><span data-stu-id="9f8d3-113">If EUDC is disabled, trying to display EUDC characters will result in missing or bad glyphs.</span></span>

<span data-ttu-id="9f8d3-114">在多會話期間，此函數只會影響目前的會話。</span><span class="sxs-lookup"><span data-stu-id="9f8d3-114">During multi-session, this function affects the current session only.</span></span>

<span data-ttu-id="9f8d3-115">建議您搭配 Windows XP SP2 或更新版本使用此函數。</span><span class="sxs-lookup"><span data-stu-id="9f8d3-115">It is recommended that you use this function with Windows XP SP2 or later.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f8d3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9f8d3-116">Requirements</span></span>



| <span data-ttu-id="9f8d3-117">需求</span><span class="sxs-lookup"><span data-stu-id="9f8d3-117">Requirement</span></span> | <span data-ttu-id="9f8d3-118">值</span><span class="sxs-lookup"><span data-stu-id="9f8d3-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9f8d3-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9f8d3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9f8d3-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f8d3-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9f8d3-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9f8d3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9f8d3-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9f8d3-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9f8d3-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="9f8d3-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="9f8d3-124"><dt>Gdi32 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9f8d3-124"><dt>Gdi32.lib</dt></span></span> </dl> |
| <span data-ttu-id="9f8d3-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9f8d3-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f8d3-126"><dt>Gdi32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f8d3-126"><dt>Gdi32.dll</dt></span></span> </dl> |



 

 




