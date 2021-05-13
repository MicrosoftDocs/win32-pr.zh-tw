---
description: 建立代表硬體元件及其相關事件處理常式的標記。 自動播放會使用此函式來允許應用程式使用自動播放事件。
title: CreateHardwareEventMoniker 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CreateHardwareEventMoniker
api_type:
- DllExport
api_location:
- Shsvcs.dll
ms.assetid: ff0ad023-42ea-4c74-adae-af55527b6ac3
ms.openlocfilehash: c22f01835f9c526e95a4330e6ad35d370421e604
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841239"
---
# <a name="createhardwareeventmoniker-function"></a><span data-ttu-id="fc9ff-104">CreateHardwareEventMoniker 函式</span><span class="sxs-lookup"><span data-stu-id="fc9ff-104">CreateHardwareEventMoniker function</span></span>

<span data-ttu-id="fc9ff-105">\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-105">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="fc9ff-106">它可能會在後續版本的 Windows 中改變或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="fc9ff-106">It might be altered or unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="fc9ff-107">建立代表硬體元件及其相關事件處理常式的標記。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-107">Creates a moniker representing a hardware component and its associated event handler.</span></span> <span data-ttu-id="fc9ff-108">自動播放會使用此函式來允許應用程式使用自動播放事件。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-108">AutoPlay uses this function to allow applications to use AutoPlay events.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc9ff-109">語法</span><span class="sxs-lookup"><span data-stu-id="fc9ff-109">Syntax</span></span>


```C++
HRESULT CreateHardwareEventMoniker(
  _In_  REFCLSID clsid,
  _In_  LPCTSTR  pszEventHandler,
  _Out_ IMoniker **ppmoniker
);
```



## <a name="parameters"></a><span data-ttu-id="fc9ff-110">參數</span><span class="sxs-lookup"><span data-stu-id="fc9ff-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc9ff-111">*clsid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc9ff-111">*clsid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc9ff-112">類型： **REFCLSID**</span><span class="sxs-lookup"><span data-stu-id="fc9ff-112">Type: **REFCLSID**</span></span>

<span data-ttu-id="fc9ff-113">標記所系結之類別的識別碼。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-113">The ID of the class to which the moniker binds.</span></span>

</dd> <dt>

<span data-ttu-id="fc9ff-114">*pszEventHandler* \[在\]</span><span class="sxs-lookup"><span data-stu-id="fc9ff-114">*pszEventHandler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fc9ff-115">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="fc9ff-115">Type: **LPCTSTR**</span></span>

<span data-ttu-id="fc9ff-116">事件處理常式的名稱。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-116">The name of the event handler.</span></span>

</dd> <dt>

<span data-ttu-id="fc9ff-117">*ppmoniker* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fc9ff-117">*ppmoniker* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fc9ff-118">類型： **[ **IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span><span class="sxs-lookup"><span data-stu-id="fc9ff-118">Type: **[**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker)\*\***</span></span>

<span data-ttu-id="fc9ff-119">接收 [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) 介面指標之指標變數的位址。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-119">The address of a pointer variable that receives the [**IMoniker**](/windows/win32/api/objidl/nn-objidl-imoniker) interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc9ff-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc9ff-120">Return value</span></span>

<span data-ttu-id="fc9ff-121">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fc9ff-121">Type: **HRESULT**</span></span>

<span data-ttu-id="fc9ff-122">如果此函式成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-122">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fc9ff-123">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc9ff-124">備註</span><span class="sxs-lookup"><span data-stu-id="fc9ff-124">Remarks</span></span>

<span data-ttu-id="fc9ff-125">註冊正在執行的應用程式時，請使用 **CreateHardwareEventMoniker** ，讓這些應用程式能夠存取自動播放事件。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-125">Use **CreateHardwareEventMoniker** when registering running applications so that those applications have access to AutoPlay events.</span></span> <span data-ttu-id="fc9ff-126">若要在執行中的應用程式中使用自動播放事件，您必須先建立新的元件來執行 [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) 介面。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-126">To use AutoPlay events in running applications, you must first create a new component that implements the [**IHWEventHandler**](/windows/desktop/api/Shobjidl/nn-shobjidl-ihweventhandler) interface.</span></span> <span data-ttu-id="fc9ff-127">使用 **處理常式** 索引鍵下特定處理常式專案的 InitCmdLine 值來初始化這個介面，因為自動播放不會呼叫 [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) 方法。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-127">Initialize this interface with the InitCmdLine value from the particular handler's entry under the **Handlers** key, because AutoPlay does not call the [**Initialize**](/windows/desktop/api/Shobjidl/nf-shobjidl-ihweventhandler-initialize) method.</span></span>

<span data-ttu-id="fc9ff-128">您應該呼叫 **CreateHardwareEventMoniker** 來取得代表您的元件和其事件處理常式的標記。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-128">You should call **CreateHardwareEventMoniker** to get a moniker that represents your component and its event handler.</span></span> <span data-ttu-id="fc9ff-129">然後，使用 *ppmoniker* 參數中所傳回的值，在執行中的物件資料表中註冊您的元件 (衰減) 如範例所示。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-129">Then, use the value returned in the *ppmoniker* parameter to register your component in the running object table (ROT) as shown in the example.</span></span>

<span data-ttu-id="fc9ff-130">請注意， **CreateHardwareEventMoniker** 並未定義在標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-130">Note that **CreateHardwareEventMoniker** is not defined in a header file.</span></span> <span data-ttu-id="fc9ff-131">若要在程式碼中使用它，您必須透過呼叫 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)來取得 Shsvcs.dll 檔案的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-131">To use it in your code, you must obtain a handle to the Shsvcs.dll file through a call to [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya).</span></span> <span data-ttu-id="fc9ff-132">然後，您可以在對 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 的呼叫中使用該控制碼，以取得 **CreateHardwareEventMoniker** 函式的實例。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-132">You then use that handle in a call to [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) to obtain an instance of the **CreateHardwareEventMoniker** function.</span></span>

<span data-ttu-id="fc9ff-133">呼叫 [**IRunningObjectTable：： Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) 需要您在登錄中輸入下列 **AppID** 資訊。</span><span class="sxs-lookup"><span data-stu-id="fc9ff-133">The call to [**IRunningObjectTable::Register**](/windows/win32/api/objidl/nf-objidl-irunningobjecttable-register) requires that you enter the following **AppID** information in the registry.</span></span>

```
HKEY_CLASSES_ROOT
   AppID
      MyApp.exe
         (Default) = MyApplication
         AppID [REG_SZ] = {Your GUID here}
```

```
HKEY_CLASSES_ROOT
   AppID
      {The same GUID here}
         (Default) = MyApplication
         RunAs = Interactive User
```

## <a name="requirements"></a><span data-ttu-id="fc9ff-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc9ff-134">Requirements</span></span>



| <span data-ttu-id="fc9ff-135">需求</span><span class="sxs-lookup"><span data-stu-id="fc9ff-135">Requirement</span></span> | <span data-ttu-id="fc9ff-136">值</span><span class="sxs-lookup"><span data-stu-id="fc9ff-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fc9ff-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc9ff-137">Minimum supported client</span></span><br/> | <span data-ttu-id="fc9ff-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc9ff-138">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="fc9ff-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc9ff-139">Minimum supported server</span></span><br/> | <span data-ttu-id="fc9ff-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fc9ff-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="fc9ff-141">標頭</span><span class="sxs-lookup"><span data-stu-id="fc9ff-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="fc9ff-142"><dt>None</dt></span><span class="sxs-lookup"><span data-stu-id="fc9ff-142"><dt>None</dt></span></span> </dl>       |
| <span data-ttu-id="fc9ff-143">DLL</span><span class="sxs-lookup"><span data-stu-id="fc9ff-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc9ff-144"><dt>Shsvcs.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc9ff-144"><dt>Shsvcs.dll</dt></span></span> </dl> |



 

 
