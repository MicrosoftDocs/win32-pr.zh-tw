---
description: 開啟 [系統] 對話方塊來要求啟用位置之裝置的使用者權限。
ms.assetid: 25b4368d-ff9d-4806-a22e-4ae0760d6f0f
title: LocationDisp. LatLongReportFactory. RequestPermissions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- LocationDisp.LatLongReportFactory.RequestPermissions
api_type:
- COM
api_location: ''
ms.openlocfilehash: ed789aca4b6c9d0db50a3e7b6cae33d55d22920c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989471"
---
# <a name="locationdisplatlongreportfactoryrequestpermissions-method"></a><span data-ttu-id="bc93c-103">LocationDisp. LatLongReportFactory. RequestPermissions 方法</span><span class="sxs-lookup"><span data-stu-id="bc93c-103">LocationDisp.LatLongReportFactory.RequestPermissions method</span></span>

<span data-ttu-id="bc93c-104">\[位置 API 物件模型可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="bc93c-104">\[The Location API object model is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="bc93c-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="bc93c-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="bc93c-106">相反地，若要從網站存取位置，請使用 [W3C 地理位置 API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="bc93c-106">Instead, to access location from a website, use the [W3C Geolocation API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)).</span></span> <span data-ttu-id="bc93c-107">若要從桌面應用程式存取位置，請使用 [**Windows. 地理位置**](/uwp/api/Windows.Devices.Geolocation) API。\]</span><span class="sxs-lookup"><span data-stu-id="bc93c-107">To access location from a desktop application, use the [**Windows.Devices.Geolocation**](/uwp/api/Windows.Devices.Geolocation) API.\]</span></span>

<span data-ttu-id="bc93c-108">開啟 [系統] 對話方塊來要求啟用位置之裝置的使用者權限。</span><span class="sxs-lookup"><span data-stu-id="bc93c-108">Opens a system dialog box to request user permission for location-enabled devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc93c-109">語法</span><span class="sxs-lookup"><span data-stu-id="bc93c-109">Syntax</span></span>


```JScript
LocationDisp.LatLongReportFactory.RequestPermissions(
  hWnd
)
```



## <a name="parameters"></a><span data-ttu-id="bc93c-110">參數</span><span class="sxs-lookup"><span data-stu-id="bc93c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc93c-111">*hWnd*</span><span class="sxs-lookup"><span data-stu-id="bc93c-111">*hWnd*</span></span> 
</dt> <dd>

<span data-ttu-id="bc93c-112">不使用此參數，應該設定為零。</span><span class="sxs-lookup"><span data-stu-id="bc93c-112">This parameter is not used and should be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc93c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="bc93c-113">Return value</span></span>

<span data-ttu-id="bc93c-114">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="bc93c-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc93c-115">備註</span><span class="sxs-lookup"><span data-stu-id="bc93c-115">Remarks</span></span>

<span data-ttu-id="bc93c-116">呼叫是同步的，且呼叫端會等候對話方塊關閉。</span><span class="sxs-lookup"><span data-stu-id="bc93c-116">The call is synchronous and the caller waits for the dialog box to be closed.</span></span>

> [!Note]  
> <span data-ttu-id="bc93c-117">如果以受保護模式執行的應用程式（例如瀏覽器協助程式物件） (BHO) 用於 Internet Explorer，則會呼叫 **RequestPermissions**，而使用者在對話方塊中選擇 [ **不要啟用此定位感應器** ] 選項，將不會啟用位置提供者，但是如果相同的使用者再次呼叫 **RequestPermissions** ，則 Windows 會再次顯示此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bc93c-117">If an application running in protected mode, such as a Browser Helper Object (BHO) for Internet Explorer, calls **RequestPermissions**, and the user chooses the **Don't enable this location sensor** option in the dialog box, the location provider will not be enabled, but Windows will display the dialog box again if **RequestPermissions** is called again by the same user.</span></span> <span data-ttu-id="bc93c-118">在受保護模式下執行的應用程式，可能會選擇不在啟動時呼叫 **RequestPermissions** ，讓使用者不會在每次應用程式啟動時看到可能的不必要對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bc93c-118">Applications that run in protected mode may choose to not call **RequestPermissions** on startup so that the user does not see a possibly unwanted dialog box each time the application starts.</span></span>

 

## <a name="examples"></a><span data-ttu-id="bc93c-119">範例</span><span class="sxs-lookup"><span data-stu-id="bc93c-119">Examples</span></span>

<span data-ttu-id="bc93c-120">如需如何使用此方法的範例，請參閱 [接聽 LatLong 報表事件](/uwp/api/Windows.Devices.Geolocation)。</span><span class="sxs-lookup"><span data-stu-id="bc93c-120">For an example of how to use this method, see [Listening for LatLong Report Events](/uwp/api/Windows.Devices.Geolocation).</span></span>

## <a name="requirements"></a><span data-ttu-id="bc93c-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc93c-121">Requirements</span></span>



| <span data-ttu-id="bc93c-122">需求</span><span class="sxs-lookup"><span data-stu-id="bc93c-122">Requirement</span></span> | <span data-ttu-id="bc93c-123">值</span><span class="sxs-lookup"><span data-stu-id="bc93c-123">Value</span></span> |
|-------------------------------------|--------------------------------------------|
| <span data-ttu-id="bc93c-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc93c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="bc93c-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bc93c-125">Windows 7 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="bc93c-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc93c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="bc93c-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="bc93c-127">None supported</span></span><br/>                  |



 

