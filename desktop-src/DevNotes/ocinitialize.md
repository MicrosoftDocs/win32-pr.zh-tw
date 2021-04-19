---
description: 初始化選用元件管理員。
ms.assetid: 9a7ddca6-a6c8-4d96-81bb-66158b83ab68
title: OcInitialize 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OcInitialize
api_type:
- DllExport
api_location:
- OcManage.dll
ms.openlocfilehash: aad102ac9881a801f693a429aab5dae07d09b5e8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999330"
---
# <a name="ocinitialize-function"></a><span data-ttu-id="dd2c4-103">OcInitialize 函式</span><span class="sxs-lookup"><span data-stu-id="dd2c4-103">OcInitialize function</span></span>

<span data-ttu-id="dd2c4-104">初始化選用元件管理員。</span><span class="sxs-lookup"><span data-stu-id="dd2c4-104">Initializes the optional component manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd2c4-105">語法</span><span class="sxs-lookup"><span data-stu-id="dd2c4-105">Syntax</span></span>


```C++
PVOID OcInitialize(
  _In_  POCM_CLIENT_CALLBACKS Callbacks,
  _In_  LPCTSTR               MasterOcInfName,
  _In_  UINT                  Flags,
  _Out_ PBOOL                 ShowError,
  _In_  PVOID                 Log
);
```



## <a name="parameters"></a><span data-ttu-id="dd2c4-106">參數</span><span class="sxs-lookup"><span data-stu-id="dd2c4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd2c4-107">*回呼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dd2c4-107">*Callbacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2c4-108">[**OCM \_ 用戶端 \_ 回呼**](ocm-client-callbacks.md)結構的指標，指定要讓 OC 管理員用來執行各種工作的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="dd2c4-108">A pointer to an [**OCM\_CLIENT\_CALLBACKS**](ocm-client-callbacks.md) structure that specifies the callback functions to be used by the OC manager to perform various tasks.</span></span>

</dd> <dt>

<span data-ttu-id="dd2c4-109">*MasterOcInfName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dd2c4-109">*MasterOcInfName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2c4-110">主要 OC .inf 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="dd2c4-110">The path of the master OC .inf file.</span></span>

</dd> <dt>

<span data-ttu-id="dd2c4-111">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="dd2c4-111">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2c4-112">這個參數可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="dd2c4-112">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="dd2c4-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT \_FORCENEWINF** (0x00000001) </span><span class="sxs-lookup"><span data-stu-id="dd2c4-113"><span id="OCINIT_FORCENEWINF"></span><span id="ocinit_forcenewinf"></span>**OCINIT\_FORCENEWINF** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="dd2c4-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT \_KILLSUBCOMPS** (0x00000002) </span><span class="sxs-lookup"><span data-stu-id="dd2c4-114"><span id="OCINIT_KILLSUBCOMPS"></span><span id="ocinit_killsubcomps"></span>**OCINIT\_KILLSUBCOMPS** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="dd2c4-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT \_RUNQUIET** (0x00000004) </span><span class="sxs-lookup"><span data-stu-id="dd2c4-115"><span id="OCINIT_RUNQUIET"></span><span id="ocinit_runquiet"></span>**OCINIT\_RUNQUIET** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="dd2c4-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT \_LANGUAGEAWARE** (0x00000008) </span><span class="sxs-lookup"><span data-stu-id="dd2c4-116"><span id="OCINIT_LANGUAGEAWARE"></span><span id="ocinit_languageaware"></span>**OCINIT\_LANGUAGEAWARE** (0x00000008)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="dd2c4-117">*ShowError* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dd2c4-117">*ShowError* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2c4-118">如果函式失敗，這個參數會指出是否要顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="dd2c4-118">If the function fails, this parameter indicates whether to display an error message.</span></span>

</dd> <dt>

<span data-ttu-id="dd2c4-119">*記錄* \[ 檔在\]</span><span class="sxs-lookup"><span data-stu-id="dd2c4-119">*Log* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dd2c4-120">記錄的控制碼。</span><span class="sxs-lookup"><span data-stu-id="dd2c4-120">A handle to the log.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dd2c4-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="dd2c4-121">Return value</span></span>

<span data-ttu-id="dd2c4-122">函數會傳回 OC 管理員內容值。</span><span class="sxs-lookup"><span data-stu-id="dd2c4-122">The function returns the OC manager context value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd2c4-123">備註</span><span class="sxs-lookup"><span data-stu-id="dd2c4-123">Remarks</span></span>

<span data-ttu-id="dd2c4-124">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="dd2c4-124">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd2c4-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd2c4-125">Requirements</span></span>



| <span data-ttu-id="dd2c4-126">需求</span><span class="sxs-lookup"><span data-stu-id="dd2c4-126">Requirement</span></span> | <span data-ttu-id="dd2c4-127">值</span><span class="sxs-lookup"><span data-stu-id="dd2c4-127">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dd2c4-128">DLL</span><span class="sxs-lookup"><span data-stu-id="dd2c4-128">DLL</span></span><br/> | <dl> <span data-ttu-id="dd2c4-129"><dt>OcManage.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd2c4-129"><dt>OcManage.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd2c4-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd2c4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd2c4-131">**OCM \_ 用戶端 \_ 回呼**</span><span class="sxs-lookup"><span data-stu-id="dd2c4-131">**OCM\_CLIENT\_CALLBACKS**</span></span>](ocm-client-callbacks.md)
</dt> <dt>

[<span data-ttu-id="dd2c4-132">**OcTerminate**</span><span class="sxs-lookup"><span data-stu-id="dd2c4-132">**OcTerminate**</span></span>](octerminate.md)
</dt> </dl>

 

 
