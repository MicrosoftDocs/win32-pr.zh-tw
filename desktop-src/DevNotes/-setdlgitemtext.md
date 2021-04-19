---
description: 在對話方塊中設定控制項的標題或文字。
ms.assetid: 84d1919e-8868-412f-bcbf-d68fe8b2cee1
title: _SetDlgItemText 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SetDlgItemText
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: 5c5b42281c127f2fe7c7935387f804a9e58b794d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981319"
---
# <a name="_setdlgitemtext-function"></a><span data-ttu-id="ffa89-103">\_SetDlgItemText 函式</span><span class="sxs-lookup"><span data-stu-id="ffa89-103">\_SetDlgItemText function</span></span>

<span data-ttu-id="ffa89-104">\[此函式是 **SetDlgItemText** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="ffa89-104">\[This function is a wrapper over the **SetDlgItemText** function.</span></span> <span data-ttu-id="ffa89-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="ffa89-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="ffa89-106">應用程式應該直接呼叫 **SetDlgItemText** 。\]</span><span class="sxs-lookup"><span data-stu-id="ffa89-106">Applications should call **SetDlgItemText** directly.\]</span></span>

<span data-ttu-id="ffa89-107">在對話方塊中設定控制項的標題或文字。</span><span class="sxs-lookup"><span data-stu-id="ffa89-107">Sets the title or text of a control in a dialog box.</span></span> <span data-ttu-id="ffa89-108">請參閱 [**SetDlgItemText**](/windows/win32/api/winuser/nf-winuser-setdlgitemtexta)。</span><span class="sxs-lookup"><span data-stu-id="ffa89-108">See [**SetDlgItemText**](/windows/win32/api/winuser/nf-winuser-setdlgitemtexta).</span></span>

## <a name="syntax"></a><span data-ttu-id="ffa89-109">語法</span><span class="sxs-lookup"><span data-stu-id="ffa89-109">Syntax</span></span>


```C++
BOOL _SetDlgItemText(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="ffa89-110">參數</span><span class="sxs-lookup"><span data-stu-id="ffa89-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffa89-111">*...*</span><span class="sxs-lookup"><span data-stu-id="ffa89-111">*...*</span></span> 
<span data-ttu-id="ffa89-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ffa89-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ffa89-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffa89-113">Requirements</span></span>



| <span data-ttu-id="ffa89-114">需求</span><span class="sxs-lookup"><span data-stu-id="ffa89-114">Requirement</span></span> | <span data-ttu-id="ffa89-115">值</span><span class="sxs-lookup"><span data-stu-id="ffa89-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa89-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ffa89-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ffa89-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ffa89-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffa89-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffa89-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa89-119">**SetDlgItemText**</span><span class="sxs-lookup"><span data-stu-id="ffa89-119">**SetDlgItemText**</span></span>](/windows/win32/api/winuser/nf-winuser-setdlgitemtexta)
</dt> </dl>

 

 
