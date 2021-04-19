---
description: PSetupGetGlobalFlags 函式是不受支援的公用程式。
ms.assetid: c993ef5d-9f4e-4643-aa9b-017c90796c8d
title: pSetupGetGlobalFlags 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- pSetupGetGlobalFlags
api_type:
- DllExport
api_location:
- Setupapi.dll
ms.openlocfilehash: 625e84e9ee88edb1ede310ec4459e89ef2e44be6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000887"
---
# <a name="psetupgetglobalflags-function"></a><span data-ttu-id="15e65-103">pSetupGetGlobalFlags 函式</span><span class="sxs-lookup"><span data-stu-id="15e65-103">pSetupGetGlobalFlags function</span></span>

<span data-ttu-id="15e65-104">\[在 Windows Vista 或 Windows Server 2008 中無法使用此功能。\]</span><span class="sxs-lookup"><span data-stu-id="15e65-104">\[This function is not available in Windows Vista or Windows Server 2008.\]</span></span>

<span data-ttu-id="15e65-105">**PSetupGetGlobalFlags** 函式是不受支援的公用程式。</span><span class="sxs-lookup"><span data-stu-id="15e65-105">The **pSetupGetGlobalFlags** function is an unsupported utility.</span></span>

## <a name="syntax"></a><span data-ttu-id="15e65-106">語法</span><span class="sxs-lookup"><span data-stu-id="15e65-106">Syntax</span></span>


```C++
VOID WINAPI pSetupGetGlobalFlags(void);
```



## <a name="parameters"></a><span data-ttu-id="15e65-107">參數</span><span class="sxs-lookup"><span data-stu-id="15e65-107">Parameters</span></span>

<span data-ttu-id="15e65-108">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="15e65-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="15e65-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="15e65-109">Return value</span></span>

<span data-ttu-id="15e65-110">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="15e65-110">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="15e65-111">備註</span><span class="sxs-lookup"><span data-stu-id="15e65-111">Remarks</span></span>

<span data-ttu-id="15e65-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="15e65-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="15e65-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="15e65-113">Requirements</span></span>



| <span data-ttu-id="15e65-114">需求</span><span class="sxs-lookup"><span data-stu-id="15e65-114">Requirement</span></span> | <span data-ttu-id="15e65-115">值</span><span class="sxs-lookup"><span data-stu-id="15e65-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="15e65-116">DLL</span><span class="sxs-lookup"><span data-stu-id="15e65-116">DLL</span></span><br/> | <dl> <span data-ttu-id="15e65-117"><dt>Setupapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15e65-117"><dt>Setupapi.dll</dt></span></span> </dl> |



 

 
