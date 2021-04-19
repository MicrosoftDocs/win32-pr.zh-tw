---
description: 為您的應用程式保存的所有設定檔設定持續性群組識別碼清單。
ms.assetid: EF83F295-CD53-45A4-B209-560B4069CA7C
title: 'WFDDisplaySinkSetPersistedGroupIDList 函式 (Wfdsink) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDSetDisplaySinkPersistedGroupIDList
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423360d7127f331fd1aa2de7f7370daebcc2b417
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106976804"
---
# <a name="wfddisplaysinksetpersistedgroupidlist-function"></a><span data-ttu-id="dde72-103">WFDDisplaySinkSetPersistedGroupIDList 函式</span><span class="sxs-lookup"><span data-stu-id="dde72-103">WFDDisplaySinkSetPersistedGroupIDList function</span></span>

<span data-ttu-id="dde72-104">為您的應用程式保存的所有設定檔設定持續性群組識別碼清單。</span><span class="sxs-lookup"><span data-stu-id="dde72-104">Sets the persisted group id list for all the profiles that are persisted by your app.</span></span> <span data-ttu-id="dde72-105">您的應用程式在每次新增或刪除其儲存體中的設定檔時，都應該呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="dde72-105">Your app should call this method every time it adds or deletes a profile from its storage.</span></span>

## <a name="syntax"></a><span data-ttu-id="dde72-106">語法</span><span class="sxs-lookup"><span data-stu-id="dde72-106">Syntax</span></span>


```C++
DWORD WINAPI WFDSetDisplaySinkPersistedGroupIDList(
  _In_ UINT32             cGroupIDList,
  _In_ DOT11_WFD_GROUP_ID *pGroupIDList
);
```



## <a name="parameters"></a><span data-ttu-id="dde72-107">參數</span><span class="sxs-lookup"><span data-stu-id="dde72-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dde72-108">*cGroupIDList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dde72-108">*cGroupIDList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde72-109">*PGroupIDList* 指向的群組識別碼計數。</span><span class="sxs-lookup"><span data-stu-id="dde72-109">The count of group ids being pointed to by *pGroupIDList*.</span></span>

</dd> <dt>

<span data-ttu-id="dde72-110">*pGroupIDList* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dde72-110">*pGroupIDList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dde72-111">*CGroupIDList* 群組識別碼陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="dde72-111">Pointer to an array of *cGroupIDList* group ids.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dde72-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dde72-112">Return value</span></span>

<span data-ttu-id="dde72-113">如果函式成功，則傳回值為「錯誤 \_ 成功」。</span><span class="sxs-lookup"><span data-stu-id="dde72-113">If the function succeeds, the return value is ERROR\_SUCCESS.</span></span>

## <a name="remarks"></a><span data-ttu-id="dde72-114">備註</span><span class="sxs-lookup"><span data-stu-id="dde72-114">Remarks</span></span>

<span data-ttu-id="dde72-115">一律會使用整個清單來呼叫這個方法，而非子集。</span><span class="sxs-lookup"><span data-stu-id="dde72-115">This method is always expected to be called with the entire list, and not a subset.</span></span> <span data-ttu-id="dde72-116">當設定檔存放區是空的時，可以使用0設定檔來呼叫此方法。</span><span class="sxs-lookup"><span data-stu-id="dde72-116">It is OK to call this method with 0 profiles when the profile store is empty.</span></span>

<span data-ttu-id="dde72-117">不屬於所提供清單的群組識別碼重新叫用將會失敗，並出現「失敗;未知的 P2P 群組」 (狀態 8) 。</span><span class="sxs-lookup"><span data-stu-id="dde72-117">A re-invoke for a group id that is not part of the provided list will fail with "Fail; unknown P2P Group"(status 8).</span></span>

## <a name="requirements"></a><span data-ttu-id="dde72-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="dde72-118">Requirements</span></span>



| <span data-ttu-id="dde72-119">需求</span><span class="sxs-lookup"><span data-stu-id="dde72-119">Requirement</span></span> | <span data-ttu-id="dde72-120">值</span><span class="sxs-lookup"><span data-stu-id="dde72-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="dde72-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dde72-121">Minimum supported client</span></span><br/> | <span data-ttu-id="dde72-122">\[僅 Windows 8.1 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dde72-122">Windows 8.1 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="dde72-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dde72-123">Minimum supported server</span></span><br/> | <span data-ttu-id="dde72-124">僅限 Windows Server 2012 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dde72-124">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dde72-125">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="dde72-125">End of client support</span></span><br/>    | <span data-ttu-id="dde72-126">Windows 10</span><span class="sxs-lookup"><span data-stu-id="dde72-126">Windows 10</span></span><br/>                                                                      |
| <span data-ttu-id="dde72-127">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="dde72-127">End of server support</span></span><br/>    | <span data-ttu-id="dde72-128">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="dde72-128">Windows Server 2016</span></span><br/>                                                             |
| <span data-ttu-id="dde72-129">標頭</span><span class="sxs-lookup"><span data-stu-id="dde72-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="dde72-130"><dt>Wfdsink。h</dt></span><span class="sxs-lookup"><span data-stu-id="dde72-130"><dt>Wfdsink.h</dt></span></span> </dl>       |
| <span data-ttu-id="dde72-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="dde72-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="dde72-132"><dt>Wifidisplay .lib</dt></span><span class="sxs-lookup"><span data-stu-id="dde72-132"><dt>Wifidisplay.lib</dt></span></span> </dl> |
| <span data-ttu-id="dde72-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dde72-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dde72-134"><dt>Wifidisplay.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dde72-134"><dt>Wifidisplay.dll</dt></span></span> </dl> |



 

 




