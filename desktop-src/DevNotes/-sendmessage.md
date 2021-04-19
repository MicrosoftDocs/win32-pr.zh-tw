---
description: 將指定的訊息傳送至視窗或視窗。
ms.assetid: aed898b3-bb48-4da2-aee7-834ae65a2d51
title: _SendMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 2b96544ee1c850886e5fa953eb902dc4a38f283d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993981"
---
# <a name="_sendmessage-function"></a><span data-ttu-id="18056-103">\_SendMessage 函式</span><span class="sxs-lookup"><span data-stu-id="18056-103">\_SendMessage function</span></span>

<span data-ttu-id="18056-104">\[此函式是 **SendMessage** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="18056-104">\[This function is a wrapper over the **SendMessage** function.</span></span> <span data-ttu-id="18056-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="18056-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="18056-106">應用程式應該直接呼叫 **SendMessage** 。\]</span><span class="sxs-lookup"><span data-stu-id="18056-106">Applications should call **SendMessage** directly.\]</span></span>

<span data-ttu-id="18056-107">將指定的訊息傳送至視窗或視窗。</span><span class="sxs-lookup"><span data-stu-id="18056-107">Sends the specified message to a window or windows.</span></span> <span data-ttu-id="18056-108">請參閱 [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage)。</span><span class="sxs-lookup"><span data-stu-id="18056-108">See [**SendMessage**](/windows/win32/api/winuser/nf-winuser-sendmessage).</span></span>

## <a name="syntax"></a><span data-ttu-id="18056-109">語法</span><span class="sxs-lookup"><span data-stu-id="18056-109">Syntax</span></span>


```C++
LRESULT _SendMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="18056-110">參數</span><span class="sxs-lookup"><span data-stu-id="18056-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18056-111">*...*</span><span class="sxs-lookup"><span data-stu-id="18056-111">*...*</span></span> 
<span data-ttu-id="18056-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="18056-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="18056-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="18056-113">Requirements</span></span>



| <span data-ttu-id="18056-114">需求</span><span class="sxs-lookup"><span data-stu-id="18056-114">Requirement</span></span> | <span data-ttu-id="18056-115">值</span><span class="sxs-lookup"><span data-stu-id="18056-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18056-116">DLL</span><span class="sxs-lookup"><span data-stu-id="18056-116">DLL</span></span><br/> | <dl> <span data-ttu-id="18056-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18056-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18056-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18056-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18056-119">**SendMessage**</span><span class="sxs-lookup"><span data-stu-id="18056-119">**SendMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-sendmessage)
</dt> </dl>

 

 
