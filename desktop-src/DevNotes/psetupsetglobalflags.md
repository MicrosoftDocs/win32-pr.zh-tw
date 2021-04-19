---
description: 停用功能。
ms.assetid: 2ea2dcfb-84e6-4f83-9afd-c3050b53f37c
title: pSetupSetGlobalFlags 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupSetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 6fcb56f26d5aea233156e0fe3dfab13099d29df7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991201"
---
# <a name="psetupsetglobalflags-function"></a><span data-ttu-id="f5a0d-103">pSetupSetGlobalFlags 函式</span><span class="sxs-lookup"><span data-stu-id="f5a0d-103">pSetupSetGlobalFlags function</span></span>

<span data-ttu-id="f5a0d-104">\[在 Windows Vista 或 Windows Server 2008 中無法使用此功能。\]</span><span class="sxs-lookup"><span data-stu-id="f5a0d-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="f5a0d-105">停用功能。</span><span class="sxs-lookup"><span data-stu-id="f5a0d-105">Disables features.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a0d-106">語法</span><span class="sxs-lookup"><span data-stu-id="f5a0d-106">Syntax</span></span>


```C++
VOID pSetupSetGlobalFlags(
  _In_ DWORD Value
);
```



## <a name="parameters"></a><span data-ttu-id="f5a0d-107">參數</span><span class="sxs-lookup"><span data-stu-id="f5a0d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a0d-108">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5a0d-108">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a0d-109">用來停用使用者介面或自動備份的旗標。</span><span class="sxs-lookup"><span data-stu-id="f5a0d-109">The flags used to disable user interface or automatic backup.</span></span>



| <span data-ttu-id="f5a0d-110">值</span><span class="sxs-lookup"><span data-stu-id="f5a0d-110">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="f5a0d-111">意義</span><span class="sxs-lookup"><span data-stu-id="f5a0d-111">Meaning</span></span>                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------|
| <span id="PSPGF_NONINTERACTIVE"></span><span id="pspgf_noninteractive"></span><dl> <span data-ttu-id="f5a0d-112"><dt>**PSPGF \_非互動式**</dt> <dt>0x004</dt></span><span class="sxs-lookup"><span data-stu-id="f5a0d-112"><dt>**PSPGF\_NONINTERACTIVE**</dt> <dt>0x004</dt></span></span> </dl> | <span data-ttu-id="f5a0d-113">設定為 [停用使用者介面]。</span><span class="sxs-lookup"><span data-stu-id="f5a0d-113">Set to disable user interface.</span></span><br/>   |
| <span id="PSPGF_NO_BACKUP"></span><span id="pspgf_no_backup"></span><dl> <span data-ttu-id="f5a0d-114"><dt>**PSPGF \_沒有 \_ 備份**</dt> <dt>0x002</dt></span><span class="sxs-lookup"><span data-stu-id="f5a0d-114"><dt>**PSPGF\_NO\_BACKUP**</dt> <dt>0x002</dt></span></span> </dl>               | <span data-ttu-id="f5a0d-115">設定為 [停用自動備份]。</span><span class="sxs-lookup"><span data-stu-id="f5a0d-115">Set to disable automatic backup.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a0d-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5a0d-116">Return value</span></span>

<span data-ttu-id="f5a0d-117">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="f5a0d-117">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5a0d-118">備註</span><span class="sxs-lookup"><span data-stu-id="f5a0d-118">Remarks</span></span>

<span data-ttu-id="f5a0d-119">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="f5a0d-119">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a0d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5a0d-120">Requirements</span></span>



| <span data-ttu-id="f5a0d-121">需求</span><span class="sxs-lookup"><span data-stu-id="f5a0d-121">Requirement</span></span> | <span data-ttu-id="f5a0d-122">值</span><span class="sxs-lookup"><span data-stu-id="f5a0d-122">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a0d-123">DLL</span><span class="sxs-lookup"><span data-stu-id="f5a0d-123">DLL</span></span><br/> | <dl> <span data-ttu-id="f5a0d-124"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5a0d-124"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
