---
description: 密碼編譯服務提供者 (CSP) 用來取得 windows 控制碼，CSP 應使用該控制碼做為顯示之任何使用者介面的父系或擁有者。
ms.assetid: 56f189e7-073b-4b42-b6ab-0147853fe6d5
title: 'CRYPT_RETURN_HWND 函式指標 (Cspdk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_RETURN_HWND
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: 32fadef6c231aa2ca63305a3da9d2142d0abe9c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971592"
---
# <a name="crypt_return_hwnd-function-pointer"></a><span data-ttu-id="c8ae3-103">CRYPT \_ RETURN \_ HWND 函數指標</span><span class="sxs-lookup"><span data-stu-id="c8ae3-103">CRYPT\_RETURN\_HWND function pointer</span></span>

<span data-ttu-id="c8ae3-104">[*密碼編譯服務提供者*](../secgloss/c-gly.md) (csp) 使用 **FuncReturnhWnd** 回呼函式，以取得 CSP 應使用的視窗控制碼，作為所顯示任何使用者介面的父系或擁有者。</span><span class="sxs-lookup"><span data-stu-id="c8ae3-104">The **FuncReturnhWnd** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to obtain the window handle that the CSP should use as the parent or owner of any user interface that is displayed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8ae3-105">語法</span><span class="sxs-lookup"><span data-stu-id="c8ae3-105">Syntax</span></span>


```C++
typedef void ( WINAPI *CRYPT_RETURN_HWND)(
  _Inout_ HWND *phWnd
);
```



## <a name="parameters"></a><span data-ttu-id="c8ae3-106">參數</span><span class="sxs-lookup"><span data-stu-id="c8ae3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c8ae3-107">*phWnd* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="c8ae3-107">*phWnd* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="c8ae3-108">接收父視窗控制碼之 **HWND** 變數的位址。</span><span class="sxs-lookup"><span data-stu-id="c8ae3-108">The address of an **HWND** variable that receives the parent window handle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c8ae3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c8ae3-109">Return value</span></span>

<span data-ttu-id="c8ae3-110">這個函式指標不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c8ae3-110">This function pointer does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8ae3-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8ae3-111">Requirements</span></span>



| <span data-ttu-id="c8ae3-112">需求</span><span class="sxs-lookup"><span data-stu-id="c8ae3-112">Requirement</span></span> | <span data-ttu-id="c8ae3-113">值</span><span class="sxs-lookup"><span data-stu-id="c8ae3-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8ae3-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c8ae3-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c8ae3-115">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8ae3-115">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c8ae3-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c8ae3-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c8ae3-117">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c8ae3-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c8ae3-118">標頭</span><span class="sxs-lookup"><span data-stu-id="c8ae3-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c8ae3-119"><dt>Cspdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="c8ae3-119"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8ae3-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8ae3-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8ae3-121">**CPAcquireCoNtext**</span><span class="sxs-lookup"><span data-stu-id="c8ae3-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="c8ae3-122">**VTableProvStruc**</span><span class="sxs-lookup"><span data-stu-id="c8ae3-122">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
