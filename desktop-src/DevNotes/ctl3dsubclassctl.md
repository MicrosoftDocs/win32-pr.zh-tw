---
description: 子類別化個別控制項，除非控制項出現在對話方塊中。
ms.assetid: 07a2bce1-4c69-4f8d-bb24-b17351f5e771
title: Ctl3dSubclassCtl 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dSubclassCtl
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 0ff6c6744c4ddda203149981218b8143fb78bce7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991168"
---
# <a name="ctl3dsubclassctl-function"></a><span data-ttu-id="fc37b-103">Ctl3dSubclassCtl 函式</span><span class="sxs-lookup"><span data-stu-id="fc37b-103">Ctl3dSubclassCtl function</span></span>

<span data-ttu-id="fc37b-104">子類別化個別控制項，除非控制項出現在對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="fc37b-104">Subclasses an individual control unless the control appears in a dialog box.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc37b-105">語法</span><span class="sxs-lookup"><span data-stu-id="fc37b-105">Syntax</span></span>


```C++
BOOL Ctl3dSubclassCtl(
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="fc37b-106">參數</span><span class="sxs-lookup"><span data-stu-id="fc37b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fc37b-107">*hwnd*</span><span class="sxs-lookup"><span data-stu-id="fc37b-107">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="fc37b-108">控制項視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="fc37b-108">A handle to the control window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fc37b-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc37b-109">Return value</span></span>

<span data-ttu-id="fc37b-110">如果成功將控制項子類別化，則傳回 **TRUE** ;否則，它會傳回 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="fc37b-110">Returns **TRUE** if the control is successfully subclassed; otherwise, it returns **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc37b-111">備註</span><span class="sxs-lookup"><span data-stu-id="fc37b-111">Remarks</span></span>

<span data-ttu-id="fc37b-112">此函數沒有相關聯的匯入程式庫或標頭檔;您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數來呼叫它。</span><span class="sxs-lookup"><span data-stu-id="fc37b-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc37b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc37b-113">Requirements</span></span>



| <span data-ttu-id="fc37b-114">需求</span><span class="sxs-lookup"><span data-stu-id="fc37b-114">Requirement</span></span> | <span data-ttu-id="fc37b-115">值</span><span class="sxs-lookup"><span data-stu-id="fc37b-115">Value</span></span> |
|----------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc37b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="fc37b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="fc37b-117"><dt>Ctl3d32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc37b-117"><dt>Ctl3d32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc37b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc37b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc37b-119">**Ctl3dUnsubclassCtl**</span><span class="sxs-lookup"><span data-stu-id="fc37b-119">**Ctl3dUnsubclassCtl**</span></span>](ctl3dunsubclassctl.md)
</dt> </dl>

 

 
