---
description: 在對話方塊中，將訊息傳送至指定的控制項。
ms.assetid: 7c91e432-662c-4dd0-980c-892ce1092077
title: _SendDlgItemMessage 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _SendDlgItemMessage
api_type:
- DllExport
api_location:
- Sqlunirl.dll
ms.openlocfilehash: ea5595ecef953d81ee947042e6265178c1feecd6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990129"
---
# <a name="_senddlgitemmessage-function"></a><span data-ttu-id="9367a-103">\_SendDlgItemMessage 函式</span><span class="sxs-lookup"><span data-stu-id="9367a-103">\_SendDlgItemMessage function</span></span>

<span data-ttu-id="9367a-104">\[此函式是 **SendDlgItemMessage** 函數的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="9367a-104">\[This function is a wrapper over the **SendDlgItemMessage** function.</span></span> <span data-ttu-id="9367a-105">這項功能可能會在未來變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="9367a-105">This function may be altered or unavailable in the future.</span></span> <span data-ttu-id="9367a-106">應用程式應該直接呼叫 **SendDlgItemMessage** 。\]</span><span class="sxs-lookup"><span data-stu-id="9367a-106">Applications should call **SendDlgItemMessage** directly.\]</span></span>

<span data-ttu-id="9367a-107">在對話方塊中，將訊息傳送至指定的控制項。</span><span class="sxs-lookup"><span data-stu-id="9367a-107">Sends a message to the specified control in a dialog box.</span></span> <span data-ttu-id="9367a-108">請參閱 [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)。</span><span class="sxs-lookup"><span data-stu-id="9367a-108">See [**SendDlgItemMessage**](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea).</span></span>

## <a name="syntax"></a><span data-ttu-id="9367a-109">語法</span><span class="sxs-lookup"><span data-stu-id="9367a-109">Syntax</span></span>


```C++
LRESULT _SendDlgItemMessage(
    ...
);
```



## <a name="parameters"></a><span data-ttu-id="9367a-110">參數</span><span class="sxs-lookup"><span data-stu-id="9367a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9367a-111">*...*</span><span class="sxs-lookup"><span data-stu-id="9367a-111">*...*</span></span> 
<span data-ttu-id="9367a-112"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="9367a-112"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="9367a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9367a-113">Requirements</span></span>



| <span data-ttu-id="9367a-114">需求</span><span class="sxs-lookup"><span data-stu-id="9367a-114">Requirement</span></span> | <span data-ttu-id="9367a-115">值</span><span class="sxs-lookup"><span data-stu-id="9367a-115">Value</span></span> |
|----------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9367a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="9367a-116">DLL</span></span><br/> | <dl> <span data-ttu-id="9367a-117"><dt>Sqlunirl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9367a-117"><dt>Sqlunirl.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9367a-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9367a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9367a-119">**SendDlgItemMessage**</span><span class="sxs-lookup"><span data-stu-id="9367a-119">**SendDlgItemMessage**</span></span>](/windows/win32/api/winuser/nf-winuser-senddlgitemmessagea)
</dt> </dl>

 

 
