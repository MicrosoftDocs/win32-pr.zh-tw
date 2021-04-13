---
description: 呼叫程式庫以取得相對於主機的安全性狀態，以及要使用的腳本或 msi。
ms.assetid: 4CCDA3B7-7661-47F6-A015-720BDEAEDBB1
title: 'WldpGetLockdownPolicy 函式 (Wldp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpGetLockdownPolicy
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: a8f5e4da11e8ce7443d9a9bab323742cfc1b3a9d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510527"
---
# <a name="wldpgetlockdownpolicy-function"></a><span data-ttu-id="cd62d-103">WldpGetLockdownPolicy 函式</span><span class="sxs-lookup"><span data-stu-id="cd62d-103">WldpGetLockdownPolicy function</span></span>

<span data-ttu-id="cd62d-104">呼叫程式庫以取得相對於主機的安全性狀態，以及要使用的腳本或 msi。</span><span class="sxs-lookup"><span data-stu-id="cd62d-104">Calls the library to get the security state relative to the host, and script or msi to be used.</span></span> <span data-ttu-id="cd62d-105">函數沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="cd62d-105">The function has no associated import library.</span></span> <span data-ttu-id="cd62d-106">您必須使用 LoadLibrary 和 GetProcAddress 函數，以動態方式連結至 wldp.dll。</span><span class="sxs-lookup"><span data-stu-id="cd62d-106">You must use the LoadLibrary and GetProcAddress functions to dynamically link to wldp.dll.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd62d-107">語法</span><span class="sxs-lookup"><span data-stu-id="cd62d-107">Syntax</span></span>


```C++
HRESULT WINAPI WldpGetLockdownPolicy(
  _In_opt_ PWLDP_HOST_INFORMATION hostInformation,
  _Out_    PDWORD                 lockdownState,
  _In_     DWORD                  lockdownFlags
);
```



## <a name="parameters"></a><span data-ttu-id="cd62d-108">參數</span><span class="sxs-lookup"><span data-stu-id="cd62d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd62d-109">*hostInformation* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="cd62d-109">*hostInformation* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="cd62d-110">[**WLDP \_ 主機 \_ 資訊**](wldp-host-information.md)結構，用來識別要評估的主機和來源檔案。</span><span class="sxs-lookup"><span data-stu-id="cd62d-110">A [**WLDP\_HOST\_INFORMATION**](wldp-host-information.md) structure identifying the host and source file to be evaluated.</span></span>

</dd> <dt>

<span data-ttu-id="cd62d-111">*lockdownState* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="cd62d-111">*lockdownState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd62d-112">提供產生的原則安全值。</span><span class="sxs-lookup"><span data-stu-id="cd62d-112">Provides the resulting policy secure value.</span></span> <span data-ttu-id="cd62d-113">如果！WLDP_LOCKDOWN_IS_OFF，則會啟用 UMCI。</span><span class="sxs-lookup"><span data-stu-id="cd62d-113">If !WLDP_LOCKDOWN_IS_OFF, then UMCI is enabled.</span></span> <span data-ttu-id="cd62d-114">您也可以檢查 WLDP_LOCKDOWN_IS_AUDIT 和 WLDP_LOCKDOWN_IS_ENFORCE，以判斷原則是否處於 AUDIT 或強制模式。</span><span class="sxs-lookup"><span data-stu-id="cd62d-114">You can also check WLDP_LOCKDOWN_IS_AUDIT and WLDP_LOCKDOWN_IS_ENFORCE to determine if a policy is in audit or enforce mode.</span></span>
</dd> <dt>

<span data-ttu-id="cd62d-115">*lockdownFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cd62d-115">*lockdownFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cd62d-116">下列旗標值是定義 WLDP \_ FLAGS \_ SKIPSIGNATUREVALIDATION 0x00000100 –設定時，略過 SaferIdentifyLevel 驗證，這會忽略腳本是否經過簽署。</span><span class="sxs-lookup"><span data-stu-id="cd62d-116">The following flag values are defined WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION 0x00000100 – when set, skip the SaferIdentifyLevel validation, which will ignore whether a script is signed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd62d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="cd62d-117">Return value</span></span>

<span data-ttu-id="cd62d-118">如果成功，則此方法會傳回，否則會傳回 \_ 失敗碼。</span><span class="sxs-lookup"><span data-stu-id="cd62d-118">This method returns S\_OK if successful or a failure code otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd62d-119">備註</span><span class="sxs-lookup"><span data-stu-id="cd62d-119">Remarks</span></span>

<span data-ttu-id="cd62d-120">使用 WLDP \_ 主機 \_ 資訊來呼叫時。 SZSOURCE = Null，會傳回主機的一般原則。</span><span class="sxs-lookup"><span data-stu-id="cd62d-120">When called with WLDP\_HOST\_INFORMATION.szSource = NULL, the generic policy for the host is returned.</span></span>

<span data-ttu-id="cd62d-121">使用 WLDP \_ 主機資訊呼叫時 \_ 。 DWHOSTID = WLDP \_ 主機 \_ 識別碼 \_ GLOBAL，WLDP \_ 主機 \_ 資訊。 szSource 必須是 Null，且函式會傳回全域系統原則。</span><span class="sxs-lookup"><span data-stu-id="cd62d-121">When called with WLDP\_HOST\_INFORMATION.dwHostId = WLDP\_HOST\_ID\_GLOBAL, WLDP\_HOST\_INFORMATION.szSource must be NULL, and the function will return the global system policy.</span></span>

<span data-ttu-id="cd62d-122">您 \_ 可以使用 >DWFLAG WLDP 旗標 \_ SKIPSIGNATUREVALIDATION 來略過 SaferIdentifyLevel () 驗證，這會忽略腳本是否經過簽署。</span><span class="sxs-lookup"><span data-stu-id="cd62d-122">The dwFlag WLDP\_FLAGS\_SKIPSIGNATUREVALIDATION can be used to skip the SaferIdentifyLevel() validation, which will ignore whether a script is signed.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd62d-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd62d-123">Requirements</span></span>



| <span data-ttu-id="cd62d-124">需求</span><span class="sxs-lookup"><span data-stu-id="cd62d-124">Requirement</span></span> | <span data-ttu-id="cd62d-125">值</span><span class="sxs-lookup"><span data-stu-id="cd62d-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cd62d-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd62d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="cd62d-127">\[僅 Windows 10 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd62d-127">Windows 10 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cd62d-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd62d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="cd62d-129">僅限 Windows Server 2016 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd62d-129">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cd62d-130">標頭</span><span class="sxs-lookup"><span data-stu-id="cd62d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd62d-131"><dt>Wldp。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd62d-131"><dt>Wldp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd62d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cd62d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd62d-133"><dt>Wldp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd62d-133"><dt>Wldp.dll</dt></span></span> </dl> |



 

 




