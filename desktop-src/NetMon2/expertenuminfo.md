---
description: EXPERTENUMINFO 結構提供專家的相關資訊。
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: 'EXPERTENUMINFO 結構 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972815"
---
# <a name="expertenuminfo-structure"></a><span data-ttu-id="2462d-103">EXPERTENUMINFO 結構</span><span class="sxs-lookup"><span data-stu-id="2462d-103">EXPERTENUMINFO structure</span></span>

<span data-ttu-id="2462d-104">**EXPERTENUMINFO** 結構提供專家的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2462d-104">The **EXPERTENUMINFO** structure provides information about the expert.</span></span> <span data-ttu-id="2462d-105">網路監視器會為結構配置記憶體，並在呼叫 [**註冊專家**](register-expert.md) 函式時將它傳遞給專家。</span><span class="sxs-lookup"><span data-stu-id="2462d-105">Network Monitor allocates memory for the structure, and passes it to the expert when it calls the [**Register Expert**](register-expert.md) function.</span></span> <span data-ttu-id="2462d-106">當專家收到結構時，就必須填寫網路監視器要求的所有資訊。</span><span class="sxs-lookup"><span data-stu-id="2462d-106">When the expert receives the structure, it must then fill-in all the information that Network Monitor requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="2462d-107">語法</span><span class="sxs-lookup"><span data-stu-id="2462d-107">Syntax</span></span>


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a><span data-ttu-id="2462d-108">成員</span><span class="sxs-lookup"><span data-stu-id="2462d-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="2462d-109">**szName**</span><span class="sxs-lookup"><span data-stu-id="2462d-109">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="2462d-110">專家的名稱。</span><span class="sxs-lookup"><span data-stu-id="2462d-110">Name of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="2462d-111">**szVendor**</span><span class="sxs-lookup"><span data-stu-id="2462d-111">**szVendor**</span></span>
</dt> <dd>

<span data-ttu-id="2462d-112">建立專家的廠商名稱。</span><span class="sxs-lookup"><span data-stu-id="2462d-112">Name of the vendor that creates the expert.</span></span>

</dd> <dt>

<span data-ttu-id="2462d-113">**szDescription**</span><span class="sxs-lookup"><span data-stu-id="2462d-113">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="2462d-114">專家的描述。</span><span class="sxs-lookup"><span data-stu-id="2462d-114">Description of the expert.</span></span> <span data-ttu-id="2462d-115">**SzDescription** 成員的值可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2462d-115">The value of the **szDescription** member may be **NULL**.</span></span> <span data-ttu-id="2462d-116">如果名稱太長，則會在預設檢視器設定中被截斷。</span><span class="sxs-lookup"><span data-stu-id="2462d-116">If the name is too long, it is truncated in the default viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="2462d-117">**版本**</span><span class="sxs-lookup"><span data-stu-id="2462d-117">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="2462d-118">此值必須為零。</span><span class="sxs-lookup"><span data-stu-id="2462d-118">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2462d-119">**旗標**</span><span class="sxs-lookup"><span data-stu-id="2462d-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="2462d-120">下列旗標描述專家。</span><span class="sxs-lookup"><span data-stu-id="2462d-120">The following flags describe the expert.</span></span>



| <span data-ttu-id="2462d-121">值</span><span class="sxs-lookup"><span data-stu-id="2462d-121">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="2462d-122">意義</span><span class="sxs-lookup"><span data-stu-id="2462d-122">Meaning</span></span>                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <span data-ttu-id="2462d-123"><dt>**可設定專家 \_ 列舉 \_ 旗標 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2462d-123"><dt>**EXPERT\_ENUM\_FLAG\_CONFIGURABLE**</dt></span></span> </dl>                                          | <span data-ttu-id="2462d-124">專家支援對 [**Configure**](configure.md) 方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="2462d-124">The expert supports calls to the [**Configure**](configure.md) method.</span></span> <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <span data-ttu-id="2462d-125"><dt>**私用的專家 \_ 列舉 \_ 旗標 \_ 檢視器 \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2462d-125"><dt>**EXPERT\_ENUM\_FLAG\_VIEWER\_PRIVATE**</dt></span></span> </dl>                                   | <span data-ttu-id="2462d-126">專家需要私人 (非共用) 事件檢視器。</span><span class="sxs-lookup"><span data-stu-id="2462d-126">The expert requires a private (non-shared) Event Viewer.</span></span> <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <span data-ttu-id="2462d-127"><dt>**專家 \_ 列舉 \_ 旗標 \_ 沒有 \_ 檢視器**</dt></span><span class="sxs-lookup"><span data-stu-id="2462d-127"><dt>**EXPERT\_ENUM\_FLAG\_NO\_VIEWER**</dt></span></span> </dl>                                                  | <span data-ttu-id="2462d-128">專家不會傳送事件通知。</span><span class="sxs-lookup"><span data-stu-id="2462d-128">The expert does not send event notifications.</span></span> <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <span data-ttu-id="2462d-129"><dt>**專家 \_ 列舉 \_ 旗標 \_ 將 \_ 我新增 \_ 至 \_ RMC \_ \_ 摘要**</dt></span><span class="sxs-lookup"><span data-stu-id="2462d-129"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_SUMMARY**</dt></span></span> </dl> | <span data-ttu-id="2462d-130">當焦點在 [摘要] 窗格中時，專家會出現在內容功能表上。</span><span class="sxs-lookup"><span data-stu-id="2462d-130">When the focus is in the summary pane, the expert appears on the context menu.</span></span> <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <span data-ttu-id="2462d-131"><dt>**專家 \_ 列舉 \_ 旗標更 \_ 詳細地將 \_ 我新增 \_ 至 \_ RMC \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="2462d-131"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_DETAIL**</dt></span></span> </dl>    | <span data-ttu-id="2462d-132">當焦點在 [詳細資料] 窗格中時，專家會出現在內容功能表上。</span><span class="sxs-lookup"><span data-stu-id="2462d-132">When the focus is in the detail pane, the expert appears on the context menu.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="2462d-133">**hExpert**</span><span class="sxs-lookup"><span data-stu-id="2462d-133">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="2462d-134">專家的控點。</span><span class="sxs-lookup"><span data-stu-id="2462d-134">Handle to the expert.</span></span> <span data-ttu-id="2462d-135">使用 **EXPERTENUMINFO** 結構來註冊專家時，會忽略參數。</span><span class="sxs-lookup"><span data-stu-id="2462d-135">When the **EXPERTENUMINFO** structure is used to register an expert, the parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="2462d-136">**szDllName**</span><span class="sxs-lookup"><span data-stu-id="2462d-136">**szDllName**</span></span>
</dt> <dd>

<span data-ttu-id="2462d-137">私用成員;請勿使用。</span><span class="sxs-lookup"><span data-stu-id="2462d-137">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="2462d-138">**hModule**</span><span class="sxs-lookup"><span data-stu-id="2462d-138">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="2462d-139">私用成員;請勿使用。</span><span class="sxs-lookup"><span data-stu-id="2462d-139">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="2462d-140">**pRegisterProc**</span><span class="sxs-lookup"><span data-stu-id="2462d-140">**pRegisterProc**</span></span>
</dt> <dd>

<span data-ttu-id="2462d-141">私用成員;請勿使用。</span><span class="sxs-lookup"><span data-stu-id="2462d-141">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="2462d-142">**pConfigProc**</span><span class="sxs-lookup"><span data-stu-id="2462d-142">**pConfigProc**</span></span>
</dt> <dd>

<span data-ttu-id="2462d-143">私用成員;請勿使用。</span><span class="sxs-lookup"><span data-stu-id="2462d-143">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="2462d-144">**pRunProc**</span><span class="sxs-lookup"><span data-stu-id="2462d-144">**pRunProc**</span></span>
</dt> <dd>

<span data-ttu-id="2462d-145">私用成員;請勿使用。</span><span class="sxs-lookup"><span data-stu-id="2462d-145">Private member; do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2462d-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="2462d-146">Requirements</span></span>



| <span data-ttu-id="2462d-147">需求</span><span class="sxs-lookup"><span data-stu-id="2462d-147">Requirement</span></span> | <span data-ttu-id="2462d-148">值</span><span class="sxs-lookup"><span data-stu-id="2462d-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="2462d-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2462d-149">Minimum supported client</span></span><br/> | <span data-ttu-id="2462d-150">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2462d-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="2462d-151">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2462d-151">Minimum supported server</span></span><br/> | <span data-ttu-id="2462d-152">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2462d-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="2462d-153">標頭</span><span class="sxs-lookup"><span data-stu-id="2462d-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="2462d-154"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="2462d-154"><dt>Netmon.h</dt></span></span> </dl> |



 

 




