---
description: 安裝新的裝置。 系統會提示使用者選取裝置。
ms.assetid: 9bdee82c-1d0a-41ea-8b42-7ad96ac37663
title: InstallNewDevice 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InstallNewDevice
api_type:
- DllExport
api_location:
- NewDev.dll
ms.openlocfilehash: 76a458ae071c61b9f1030aad535c4d4c6a31078c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111173"
---
# <a name="installnewdevice-function"></a><span data-ttu-id="e01d1-104">InstallNewDevice 函式</span><span class="sxs-lookup"><span data-stu-id="e01d1-104">InstallNewDevice function</span></span>

<span data-ttu-id="e01d1-105">安裝新的裝置。</span><span class="sxs-lookup"><span data-stu-id="e01d1-105">Installs a new device.</span></span> <span data-ttu-id="e01d1-106">系統會提示使用者選取裝置。</span><span class="sxs-lookup"><span data-stu-id="e01d1-106">The user is prompted to select the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="e01d1-107">語法</span><span class="sxs-lookup"><span data-stu-id="e01d1-107">Syntax</span></span>


```C++
BOOL WINAPI InstallNewDevice(
  _In_  HWND   hwndParent,
  _In_  LPGUID ClassGuid,
  _Out_ PDWORD pReboot
);
```



## <a name="parameters"></a><span data-ttu-id="e01d1-108">參數</span><span class="sxs-lookup"><span data-stu-id="e01d1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e01d1-109">*hwndParent* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e01d1-109">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e01d1-110">最上層視窗的控制碼，可用於任何必要的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="e01d1-110">A handle to the top-level window to be used for any required user interface.</span></span>

</dd> <dt>

<span data-ttu-id="e01d1-111">*ClassGuid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e01d1-111">*ClassGuid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e01d1-112">類別 **GUID** 的指標。</span><span class="sxs-lookup"><span data-stu-id="e01d1-112">A pointer to a class **GUID**.</span></span> <span data-ttu-id="e01d1-113">這是選擇性參數。</span><span class="sxs-lookup"><span data-stu-id="e01d1-113">This parameter is optional.</span></span> <span data-ttu-id="e01d1-114">如果此參數為 **Null**，則使用者會在 [偵測選擇] 頁面上啟動。</span><span class="sxs-lookup"><span data-stu-id="e01d1-114">If this parameter is **NULL**, the user starts at the detection choice page.</span></span> <span data-ttu-id="e01d1-115">如果此參數為 **guid \_ Null** 或 **guid \_ DEVCLASS \_ UNKNOWN**，則使用者會在 [類別選取] 頁面上啟動。</span><span class="sxs-lookup"><span data-stu-id="e01d1-115">If this parameter is **GUID\_NULL** or **GUID\_DEVCLASS\_UNKNOWN**, the user starts at the class selection page.</span></span>

</dd> <dt>

<span data-ttu-id="e01d1-116">*啟動* \[ 前擴展\]</span><span class="sxs-lookup"><span data-stu-id="e01d1-116">*pReboot* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e01d1-117">接收重新開機狀態之變數的指標。</span><span class="sxs-lookup"><span data-stu-id="e01d1-117">A pointer to a variable that receives the reboot status.</span></span> <span data-ttu-id="e01d1-118">此參數可以是 **di \_ NEEDRESTART** 或 **di \_ NEEDREBOOT**。</span><span class="sxs-lookup"><span data-stu-id="e01d1-118">This parameter can be **DI\_NEEDRESTART** or **DI\_NEEDREBOOT**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e01d1-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="e01d1-119">Return value</span></span>

<span data-ttu-id="e01d1-120">如果函式成功，則傳回非零的值。</span><span class="sxs-lookup"><span data-stu-id="e01d1-120">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="e01d1-121">如果此函式失敗，則傳回值為零。</span><span class="sxs-lookup"><span data-stu-id="e01d1-121">If the function fails, the return value is zero.</span></span> <span data-ttu-id="e01d1-122">若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="e01d1-122">To get extended error information, call [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="e01d1-123">備註</span><span class="sxs-lookup"><span data-stu-id="e01d1-123">Remarks</span></span>

<span data-ttu-id="e01d1-124">此函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="e01d1-124">This function has no associated import library.</span></span> <span data-ttu-id="e01d1-125">您必須使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 NewDev.dll。</span><span class="sxs-lookup"><span data-stu-id="e01d1-125">You must use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to NewDev.dll.</span></span>

## <a name="requirements"></a><span data-ttu-id="e01d1-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="e01d1-126">Requirements</span></span>



| <span data-ttu-id="e01d1-127">需求</span><span class="sxs-lookup"><span data-stu-id="e01d1-127">Requirement</span></span> | <span data-ttu-id="e01d1-128">值</span><span class="sxs-lookup"><span data-stu-id="e01d1-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e01d1-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e01d1-129">Minimum supported client</span></span><br/> | <span data-ttu-id="e01d1-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e01d1-130">Windows XP</span></span><br/>                                                                 |
| <span data-ttu-id="e01d1-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e01d1-131">Minimum supported server</span></span><br/> | <span data-ttu-id="e01d1-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e01d1-132">Windows Server 2003</span></span><br/>                                                        |
| <span data-ttu-id="e01d1-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e01d1-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e01d1-134"><dt>NewDev.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e01d1-134"><dt>NewDev.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e01d1-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e01d1-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e01d1-136">裝置管理函式</span><span class="sxs-lookup"><span data-stu-id="e01d1-136">Device Management Functions</span></span>](device-management-functions.md)
</dt> </dl>

 

