---
description: 安裝指定的系統元件。
ms.assetid: f4b7b8e5-b392-4208-9f56-b343974e05ff
title: IcfgInstallInetComponents 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IcfgInstallInetComponents
api_type:
- DllExport
api_location:
- Icfgnt5.dll
ms.openlocfilehash: 649b1fa73bcdd83d7fc01d5a4df9a198168a3f1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995723"
---
# <a name="icfginstallinetcomponents-function"></a><span data-ttu-id="1a754-103">IcfgInstallInetComponents 函式</span><span class="sxs-lookup"><span data-stu-id="1a754-103">IcfgInstallInetComponents function</span></span>

<span data-ttu-id="1a754-104">安裝指定的系統元件。</span><span class="sxs-lookup"><span data-stu-id="1a754-104">Installs the system components specified.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a754-105">語法</span><span class="sxs-lookup"><span data-stu-id="1a754-105">Syntax</span></span>


```C++
HRESULT IcfgInstallInetComponents(
   HWND   hwndParent,
   DWORD  dwfOptions,
   LPBOOL lpfNeedsRestart
);
```



## <a name="parameters"></a><span data-ttu-id="1a754-106">參數</span><span class="sxs-lookup"><span data-stu-id="1a754-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a754-107">*hwndParent*</span><span class="sxs-lookup"><span data-stu-id="1a754-107">*hwndParent*</span></span> 
</dt> <dd>

<span data-ttu-id="1a754-108">父視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1a754-108">A handle to the parent window.</span></span>

</dd> <dt>

<span data-ttu-id="1a754-109">*dwfOptions*</span><span class="sxs-lookup"><span data-stu-id="1a754-109">*dwfOptions*</span></span> 
</dt> <dd>

<span data-ttu-id="1a754-110">下列旗標的組合，可控制安裝和設定。</span><span class="sxs-lookup"><span data-stu-id="1a754-110">A combination of the following flags that control the installation and configuration.</span></span>



| <span data-ttu-id="1a754-111">值</span><span class="sxs-lookup"><span data-stu-id="1a754-111">Value</span></span>                                                                                                                                                                                                                                  | <span data-ttu-id="1a754-112">意義</span><span class="sxs-lookup"><span data-stu-id="1a754-112">Meaning</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <span id="ICFG_INSTALLMAIL"></span><span id="icfg_installmail"></span><dl> <span data-ttu-id="1a754-113"><dt>**ICFG \_INSTALLMAIL**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="1a754-113"><dt>**ICFG\_INSTALLMAIL**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="1a754-114">安裝 Exchange 和網際網路郵件。</span><span class="sxs-lookup"><span data-stu-id="1a754-114">Install Exchange and Internet mail.</span></span><br/> |
| <span id="ICFG_INSTALLRAS"></span><span id="icfg_installras"></span><dl> <span data-ttu-id="1a754-115"><dt>**ICFG \_INSTALLRAS**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="1a754-115"><dt>**ICFG\_INSTALLRAS**</dt> <dt>0x00000002</dt></span></span> </dl>    | <span data-ttu-id="1a754-116">如有需要，請安裝 RAS () 。</span><span class="sxs-lookup"><span data-stu-id="1a754-116">Install RAS (if needed).</span></span><br/>            |
| <span id="ICFG_INSTALLTCP"></span><span id="icfg_installtcp"></span><dl> <span data-ttu-id="1a754-117"><dt>**ICFG \_INSTALLTCP**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="1a754-117"><dt>**ICFG\_INSTALLTCP**</dt> <dt>0x00000001</dt></span></span> </dl>    | <span data-ttu-id="1a754-118">如有需要，請將 TCP/IP (安裝) 。</span><span class="sxs-lookup"><span data-stu-id="1a754-118">Install TCP/IP (if needed).</span></span><br/>         |



 

</dd> <dt>

<span data-ttu-id="1a754-119">*lpfNeedsRestart*</span><span class="sxs-lookup"><span data-stu-id="1a754-119">*lpfNeedsRestart*</span></span> 
</dt> <dd>

<span data-ttu-id="1a754-120">如果這個值不是 **Null**，則在傳回時，只有在必須重新開機 Windows 才能完成安裝時，才會傳回 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="1a754-120">If this value is non-**NULL**, on return it will be **TRUE** only if Windows must be restarted to complete the installation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a754-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="1a754-121">Return value</span></span>

<span data-ttu-id="1a754-122">傳回 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="1a754-122">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1a754-123">如果沒有發生錯誤，則會傳回 **錯誤 \_ 成功** 碼。</span><span class="sxs-lookup"><span data-stu-id="1a754-123">If no errors occur, it returns the **ERROR\_SUCCESS** code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a754-124">備註</span><span class="sxs-lookup"><span data-stu-id="1a754-124">Remarks</span></span>

<span data-ttu-id="1a754-125">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="1a754-125">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a754-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1a754-126">Requirements</span></span>



| <span data-ttu-id="1a754-127">需求</span><span class="sxs-lookup"><span data-stu-id="1a754-127">Requirement</span></span> | <span data-ttu-id="1a754-128">值</span><span class="sxs-lookup"><span data-stu-id="1a754-128">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1a754-129">DLL</span><span class="sxs-lookup"><span data-stu-id="1a754-129">DLL</span></span><br/> | <dl> <span data-ttu-id="1a754-130"><dt>Icfgnt5.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a754-130"><dt>Icfgnt5.dll</dt></span></span> </dl> |



 

 
