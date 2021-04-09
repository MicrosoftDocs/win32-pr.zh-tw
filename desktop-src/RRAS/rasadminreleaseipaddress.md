---
title: RasAdminReleaseIpAddress 回呼函式
description: RasAdminReleaseIpAddress 函式是由協力廠商 RAS 伺服器管理 DLL 匯出的應用程式定義函數。
ms.assetid: 86fd9173-f158-4de5-8166-483a652a52cc
keywords:
- RasAdminReleaseIpAddress 回呼函式 RAS
topic_type:
- apiref
api_name:
- RasAdminReleaseIpAddress
api_type:
- UserDefined
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d58c162ebc6d340b9bd913407bc00aac87e208e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682986"
---
# <a name="rasadminreleaseipaddress-callback-function"></a><span data-ttu-id="a4379-104">RasAdminReleaseIpAddress 回呼函式</span><span class="sxs-lookup"><span data-stu-id="a4379-104">RasAdminReleaseIpAddress callback function</span></span>

<span data-ttu-id="a4379-105">\[**RasAdminReleaseIpAddress** 函式可用於 Windows NT 4.0，並在後續版本中無法使用。</span><span class="sxs-lookup"><span data-stu-id="a4379-105">\[The **RasAdminReleaseIpAddress** function is available for use in Windows NT 4.0 and is unavailable in subsequent versions.</span></span> <span data-ttu-id="a4379-106">相反地，請使用 [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress)。\]</span><span class="sxs-lookup"><span data-stu-id="a4379-106">Instead, use [**MprAdminReleaseIpAddress**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminreleaseipaddress).\]</span></span>

<span data-ttu-id="a4379-107">**RasAdminReleaseIpAddress** 函式是由協力廠商 RAS 伺服器管理 DLL 匯出的應用程式定義函數。</span><span class="sxs-lookup"><span data-stu-id="a4379-107">The **RasAdminReleaseIpAddress** function is an application-defined function that is exported by a third-party RAS server administration DLL.</span></span> <span data-ttu-id="a4379-108">RAS 會呼叫此函式，以通知 DLL 遠端用戶端已中斷連線，而且應該釋放 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a4379-108">RAS calls this function to notify the DLL that the remote client was disconnected and that the IP address should be released.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4379-109">語法</span><span class="sxs-lookup"><span data-stu-id="a4379-109">Syntax</span></span>


```C++
void CALLBACK RasAdminReleaseIpAddress(
  _In_ WCHAR  *lpszUserName,
  _In_ WCHAR  *lpszPortName,
  _In_ IPADDR *pipAddress
);
```



## <a name="parameters"></a><span data-ttu-id="a4379-110">參數</span><span class="sxs-lookup"><span data-stu-id="a4379-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a4379-111">*lpszUserName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4379-111">*lpszUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4379-112">指定以 null 終止之 Unicode 字串的指標，此字串會指定先前使用 [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) 函式取得 IP 位址之遠端使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="a4379-112">Specifies the pointer to a null-terminated Unicode string that specifies the name of a remote user for whom an IP address was previously obtained using the [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a4379-113">*lpszPortName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4379-113">*lpszPortName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4379-114">以 null 結束的 Unicode 字串指標，指定 *lpszUserName* 指定之使用者所連接的埠名稱。</span><span class="sxs-lookup"><span data-stu-id="a4379-114">Pointer to a null-terminated Unicode string that specifies the name of the port on which the user specified by *lpszUserName* is connected.</span></span>

</dd> <dt>

<span data-ttu-id="a4379-115">*pipAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a4379-115">*pipAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a4379-116">**IPADDR** 變數的指標，此變數會指定在先前呼叫 [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md)時為此使用者傳回的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a4379-116">Pointer to an **IPADDR** variable that specifies the IP address returned for this user in a previous call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a4379-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4379-117">Return value</span></span>

<span data-ttu-id="a4379-118">此函數沒有任何延伸的錯誤資訊;不要呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)。</span><span class="sxs-lookup"><span data-stu-id="a4379-118">There is no extended error information for this function; do no call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="a4379-119">備註</span><span class="sxs-lookup"><span data-stu-id="a4379-119">Remarks</span></span>

<span data-ttu-id="a4379-120">只有當應用 **程式在先前** 呼叫 *lpszUserName* 參數所指定的 [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) *時，才* 會呼叫 **RasAdminReleaseIpAddress** 函式。</span><span class="sxs-lookup"><span data-stu-id="a4379-120">The RAS server calls the **RasAdminReleaseIpAddress** function only if the application returned **TRUE** in the *bNotifyRelease* parameter during the earlier call to [**RasAdminGetIpAddressForUser**](rasadmingetipaddressforuser.md) for the user specified by the *lpszUserName* parameter.</span></span>

<span data-ttu-id="a4379-121">協力廠商 RAS 管理 DLL 的安裝程式必須在登錄中的下列機碼底下提供資訊，向 RAS 註冊 DLL：</span><span class="sxs-lookup"><span data-stu-id="a4379-121">The setup program for a third-party RAS administration DLL must register the DLL with RAS by providing information under the following key in the registry:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="a4379-122">若要註冊 DLL，請在此機碼下設定下列值。</span><span class="sxs-lookup"><span data-stu-id="a4379-122">To register the DLL, set the following values under this key.</span></span>



| <span data-ttu-id="a4379-123">值名稱</span><span class="sxs-lookup"><span data-stu-id="a4379-123">Value name</span></span>    | <span data-ttu-id="a4379-124">值資料</span><span class="sxs-lookup"><span data-stu-id="a4379-124">Value data</span></span>                                                                    |
|---------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="a4379-125">*DisplayName*</span><span class="sxs-lookup"><span data-stu-id="a4379-125">*DisplayName*</span></span> | <span data-ttu-id="a4379-126">**REG \_ SZ** 字串，其中包含 DLL 的使用者易記顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a4379-126">A **REG\_SZ** string that contains the user-friendly display name of the DLL.</span></span> |
| <span data-ttu-id="a4379-127">*DLLPath*</span><span class="sxs-lookup"><span data-stu-id="a4379-127">*DLLPath*</span></span>     | <span data-ttu-id="a4379-128">**REG \_ SZ** 字串，其中包含 DLL 的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="a4379-128">A **REG\_SZ** string that contains the full path of the DLL.</span></span>                  |



 

<span data-ttu-id="a4379-129">例如，名為 ProElectron，Inc. 之虛構公司的 RAS 管理 DLL 的登錄專案可能是：</span><span class="sxs-lookup"><span data-stu-id="a4379-129">For example, the registry entry for a RAS administration DLL from a fictional company named ProElectron, Inc. might be:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         RAS
            AdminDll
```

<span data-ttu-id="a4379-130">*DisplayName*： **reg \_ Sz** ： ProElectron RAS 管理 DLL *DLLPath*： **reg \_ sz** ： C： \\ nt \\ system32 \\ntwkadm.dll</span><span class="sxs-lookup"><span data-stu-id="a4379-130">*DisplayName*: **REG\_SZ** : ProElectron RAS Admin DLL *DLLPath*: **REG\_SZ** : C:\\nt\\system32\\ntwkadm.dll</span></span>

<span data-ttu-id="a4379-131">RAS 系統管理 DLL 的安裝程式也應該提供移除/卸載功能。</span><span class="sxs-lookup"><span data-stu-id="a4379-131">The setup program for a RAS administration DLL should also provide remove/uninstall functionality.</span></span> <span data-ttu-id="a4379-132">如果使用者移除 DLL，安裝程式應該刪除 DLL 的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="a4379-132">If a user removes the DLL, the setup program should delete the DLL's registry entries.</span></span>

 

 