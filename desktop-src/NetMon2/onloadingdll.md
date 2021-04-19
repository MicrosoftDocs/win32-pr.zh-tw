---
description: 載入監視 DLL。
ms.assetid: 6de2750f-3f12-4c0a-af8d-3ebd227fa123
title: 'OnLoadingDLL 函式 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnLoadingDLL
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: b2d9d728065818b1e94fa436f4d1e9b62dbeb5cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973497"
---
# <a name="onloadingdll-function"></a><span data-ttu-id="11225-103">OnLoadingDLL 函式</span><span class="sxs-lookup"><span data-stu-id="11225-103">OnLoadingDLL function</span></span>

<span data-ttu-id="11225-104">**OnLoadingDLL** 函式會載入監視器 DLL。</span><span class="sxs-lookup"><span data-stu-id="11225-104">The **OnLoadingDLL** function loads the monitor DLL.</span></span>

## <a name="syntax"></a><span data-ttu-id="11225-105">語法</span><span class="sxs-lookup"><span data-stu-id="11225-105">Syntax</span></span>


```C++
HRESULT OnLoadingDLL(
  _Inout_ HBLOB hFilterBlob,
  _In_    DWORD *pCreateFlags,
  _Out_   char  **ppDefaultName,
  _Out_   char  **ppDescription,
  _Out_   char  **ppDefaultScript,
  _Out_   char  **ppDefaultConfig
);
```



## <a name="parameters"></a><span data-ttu-id="11225-106">參數</span><span class="sxs-lookup"><span data-stu-id="11225-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="11225-107">*hFilterBlob* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="11225-107">*hFilterBlob* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="11225-108">MCSVC 用來比對具有可用 Nic 之監視的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="11225-108">A BLOB that the MCSVC uses to match a monitor with available NICs.</span></span> <span data-ttu-id="11225-109">此參數一律包含 [IRTC](irtc.md) 介面的要求，因此大部分的監視器都不需要將任何專案新增至 BLOB。</span><span class="sxs-lookup"><span data-stu-id="11225-109">This parameter always contains a request for an [IRTC](irtc.md) interface, so most monitors do not need to add any entries to the BLOB.</span></span> <span data-ttu-id="11225-110">不過，自訂監視可以新增額外的篩選準則 (例如，MAC 類型必須是乙太網路) 。</span><span class="sxs-lookup"><span data-stu-id="11225-110">However, a custom monitor can add additional filter criteria (for example, that the MAC type must be Ethernet).</span></span>

</dd> <dt>

<span data-ttu-id="11225-111">*pCreateFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="11225-111">*pCreateFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="11225-112">旗標，指出 MCSVC 如何控制監視的建立。</span><span class="sxs-lookup"><span data-stu-id="11225-112">The flags that indicate how the MCSVC controls the creation of a monitor.</span></span> <span data-ttu-id="11225-113">此參數必須是下列其中一個值：</span><span class="sxs-lookup"><span data-stu-id="11225-113">This parameter must be one of the following values:</span></span>



| <span data-ttu-id="11225-114">值</span><span class="sxs-lookup"><span data-stu-id="11225-114">Value</span></span>                                                                                                                                                                                                            | <span data-ttu-id="11225-115">意義</span><span class="sxs-lookup"><span data-stu-id="11225-115">Meaning</span></span>                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MCS_CREATE_ONE_PER_NETCARD"></span><span id="mcs_create_one_per_netcard"></span><dl> <span data-ttu-id="11225-116"><dt>**MCS \_ 為 \_ \_ 每個 \_ 網卡建立一個**</dt></span><span class="sxs-lookup"><span data-stu-id="11225-116"><dt>**MCS\_CREATE\_ONE\_PER\_NETCARD**</dt></span></span> </dl>          | <span data-ttu-id="11225-117">MCSVC 可確保每個 NIC 都只會有一個此監視實例存在。</span><span class="sxs-lookup"><span data-stu-id="11225-117">The MCSVC ensures that only one instance of this monitor exists for each NIC.</span></span> <span data-ttu-id="11225-118">只有當第一個實例被終結時，才能建立第二個實例。</span><span class="sxs-lookup"><span data-stu-id="11225-118">A second instance can be created only if the first one is destroyed.</span></span><br/> |
| <span id="MCS_CREATE_CONFIGS_BY_DEFAULT"></span><span id="mcs_create_configs_by_default"></span><dl> <span data-ttu-id="11225-119"><dt>**MCS \_ 預設會建立 \_ \_ \_ 設置**</dt></span><span class="sxs-lookup"><span data-stu-id="11225-119"><dt>**MCS\_CREATE\_CONFIGS\_BY\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="11225-120">如果監視器具有預設內部設定，則在建立實例之前，MCSVC 不需要使用者設定監視。</span><span class="sxs-lookup"><span data-stu-id="11225-120">If the monitor has a default internal configuration, the MCSVC does not require the user to configure the monitor before the instance is created.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="11225-121">*ppDefaultName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="11225-121">*ppDefaultName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11225-122">指標，指向監視的預設名稱的位址。</span><span class="sxs-lookup"><span data-stu-id="11225-122">A pointer to a pointer to the address of the default name of the monitor.</span></span> <span data-ttu-id="11225-123">建立監視的實例時，MCSVC 會使用預設名稱。</span><span class="sxs-lookup"><span data-stu-id="11225-123">The MCSVC uses the default name when creating instances of the monitor.</span></span>

<span data-ttu-id="11225-124">例如，如果傳回的預設名稱是「路由器監視器」，第一個監視實例會是「路由器監視器1」，第二個則是「RouterMonitor2」，依此類推。</span><span class="sxs-lookup"><span data-stu-id="11225-124">For example, if the returned default name is "Router Monitor", the first monitor instance would be "Router Monitor 1", the second would be "RouterMonitor2, and so on.</span></span> <span data-ttu-id="11225-125">如果傳回 **Null** ，則 MCSVC 會使用 DLL 的名稱。</span><span class="sxs-lookup"><span data-stu-id="11225-125">If **NULL** is returned, the MCSVC uses the name of the DLL.</span></span>

</dd> <dt>

<span data-ttu-id="11225-126">*ppDescription* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="11225-126">*ppDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11225-127">指向監視之描述位址的指標。</span><span class="sxs-lookup"><span data-stu-id="11225-127">A pointer to a pointer to the address of the description of the monitor.</span></span> <span data-ttu-id="11225-128">描述會傳遞至監視器控制工具，此工具會使用描述向使用者指出監視器是否存在。</span><span class="sxs-lookup"><span data-stu-id="11225-128">The description is passed to the Monitor Control Tool, which uses the description to indicate to the user that the monitor exists.</span></span> <span data-ttu-id="11225-129">這個參數可以傳回 **Null**。</span><span class="sxs-lookup"><span data-stu-id="11225-129">This parameter can return **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="11225-130">*ppDefaultScript* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="11225-130">*ppDefaultScript* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11225-131">指標，指向用來設定監視之預設 HTML 表單腳本的位址。</span><span class="sxs-lookup"><span data-stu-id="11225-131">A pointer to a pointer to the address of the default HTML Form script used to configure the monitor.</span></span> <span data-ttu-id="11225-132">雖然監視的實例可以改變自己的腳本，但大部分的監視器只會從檔案載入腳本一次。</span><span class="sxs-lookup"><span data-stu-id="11225-132">Although the instances of the monitor can alter their own script, most monitors simply load their script once, from a file.</span></span> <span data-ttu-id="11225-133">*PpDefaultScript* 的值可以是 **Null**;不過，您無法從外部設定監視，也可以稍後再提供腳本。</span><span class="sxs-lookup"><span data-stu-id="11225-133">The value of *ppDefaultScript* can be **NULL**; however, then either the monitor cannot be externally configured, or it must supply a script later.</span></span> <span data-ttu-id="11225-134">在這裡提供預設腳本會更有效率。</span><span class="sxs-lookup"><span data-stu-id="11225-134">It is more efficient to supply a default script here.</span></span>

</dd> <dt>

<span data-ttu-id="11225-135">*ppDefaultConfig* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="11225-135">*ppDefaultConfig* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="11225-136">建立時用於設定監視之預設字串的位址。</span><span class="sxs-lookup"><span data-stu-id="11225-136">The address of the default string used to configure the monitor when it is created.</span></span> <span data-ttu-id="11225-137">這個參數可以設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="11225-137">This parameter can be set to **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="11225-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="11225-138">Return value</span></span>

<span data-ttu-id="11225-139">如果函式成功，則傳回值為 S \_ OK; 這與 >aad-userreadusingalternativesecurityid-noerror 相同。</span><span class="sxs-lookup"><span data-stu-id="11225-139">If the function is successful, the return value is S\_OK; which is the same as NOERROR.</span></span>

<span data-ttu-id="11225-140">如果函式不成功，MCSVC 會從其所有清單中省略指定的監視器;之後，就無法建立此類型的監視。</span><span class="sxs-lookup"><span data-stu-id="11225-140">If the function is unsuccessful, the MCSVC omits the specified monitor from all its lists; after, no monitor of this type can be created.</span></span>

## <a name="remarks"></a><span data-ttu-id="11225-141">備註</span><span class="sxs-lookup"><span data-stu-id="11225-141">Remarks</span></span>

<span data-ttu-id="11225-142">**OnLoadingDLL** 函式會在第一次載入 DLL 時，由 MCSVC 呼叫一次。</span><span class="sxs-lookup"><span data-stu-id="11225-142">The **OnLoadingDLL** function is called once by the MCSVC, when it first loads the DLL.</span></span> <span data-ttu-id="11225-143">然後，DLL 會提供預設值，在建立監視的實例時，MCSVC 會使用此值。</span><span class="sxs-lookup"><span data-stu-id="11225-143">The DLL then provides the default values that will be used by the MCSVC when creating an instance of a monitor.</span></span>

<span data-ttu-id="11225-144">監視器必須配置傳回給 MCSVC 的字串所需的所有記憶體。</span><span class="sxs-lookup"><span data-stu-id="11225-144">The monitor must allocate all the necessary memory for the strings returned to the MCSVC.</span></span> <span data-ttu-id="11225-145">傳回時，MCSVC 會建立所有字串的複本，且不會嘗試釋放傳回的字串。</span><span class="sxs-lookup"><span data-stu-id="11225-145">On return, the MCSVC makes copies of all the strings and will not attempt to free the returned strings.</span></span>

<span data-ttu-id="11225-146">監視器應使用 BLOB 協助程式函數來改變篩選 BLOB。</span><span class="sxs-lookup"><span data-stu-id="11225-146">The monitor should use BLOB helper functions to alter the filter BLOB.</span></span>

## <a name="requirements"></a><span data-ttu-id="11225-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="11225-147">Requirements</span></span>



| <span data-ttu-id="11225-148">需求</span><span class="sxs-lookup"><span data-stu-id="11225-148">Requirement</span></span> | <span data-ttu-id="11225-149">值</span><span class="sxs-lookup"><span data-stu-id="11225-149">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="11225-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="11225-150">Minimum supported client</span></span><br/> | <span data-ttu-id="11225-151">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11225-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="11225-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="11225-152">Minimum supported server</span></span><br/> | <span data-ttu-id="11225-153">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="11225-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="11225-154">標頭</span><span class="sxs-lookup"><span data-stu-id="11225-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="11225-155"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="11225-155"><dt>Netmon.h</dt></span></span> </dl> |



 

 




