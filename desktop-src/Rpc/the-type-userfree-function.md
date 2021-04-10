---
title: Type_UserFree 函式
description: 型 \_ 別 UserFree 函式是 \ 網路 \_ 封送處理 \ 和 \ 使用者 \_ 封送處理 \ 屬性的 helper 函數。
ms.assetid: cc83a074-ea6c-432a-92fe-6397a6dc3c3c
keywords:
- type_UserFree
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e923388b37a39a325c0868deca7e7926a3d7705
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682393"
---
# <a name="the-type_userfree-function"></a><span data-ttu-id="220f2-104">型別 \_ UserFree 函式</span><span class="sxs-lookup"><span data-stu-id="220f2-104">The type\_UserFree Function</span></span>

<span data-ttu-id="220f2-105">**<type> \_ UserFree** 函式是適用于 \[ [有線 \_ 封送](/windows/desktop/Midl/wire-marshal)處理 \] 和 \[ [使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理屬性的 helper 函數 \] 。</span><span class="sxs-lookup"><span data-stu-id="220f2-105">The **<type>\_UserFree** function is a helper function for the \[ [wire\_marshal](/windows/desktop/Midl/wire-marshal)\] and \[ [user\_marshal](/windows/desktop/Midl/user-marshal)\] attributes.</span></span> <span data-ttu-id="220f2-106">Stub 會呼叫這個函式來釋放伺服器端的資料。</span><span class="sxs-lookup"><span data-stu-id="220f2-106">The stubs call this function to free the data on the server side.</span></span> <span data-ttu-id="220f2-107">函式定義如下：</span><span class="sxs-lookup"><span data-stu-id="220f2-107">The function is defined as:</span></span>

``` syntax
void __RPC_USER  <type>_UserFree(
    unsigned long __RPC_FAR * pFlags,
    <type_name>  __RPC_FAR *  pMyObj );
```

<span data-ttu-id="220f2-108">函 <type> 式名稱中的，表示在 **\[ 有線 \_ 封送 \]** 處理或 **\[ 使用者 \_ 封 \] 送** 處理類型定義中指定的 userm 類型。</span><span class="sxs-lookup"><span data-stu-id="220f2-108">The <type> in the function name means the userm-type specified in the **\[wire\_marshal\]** or **\[user\_marshal\]** type definition.</span></span>

<span data-ttu-id="220f2-109">*PFlags* 參數是不 **帶正負** 號的長旗標欄位的指標。</span><span class="sxs-lookup"><span data-stu-id="220f2-109">The *pFlags* parameter is a pointer to an **unsigned long** flag field.</span></span> <span data-ttu-id="220f2-110">旗標的上半部包含憑證 DCE 針對浮點數、位元組順序和字元標記法所定義的 NDR 資料表示旗標。</span><span class="sxs-lookup"><span data-stu-id="220f2-110">The upper word of the flag contains NDR data representation flags as defined by OSF DCE for floating point, byte order, and character representations.</span></span> <span data-ttu-id="220f2-111">下方的單字包含由 COM 通道所定義的封送處理內容旗標。</span><span class="sxs-lookup"><span data-stu-id="220f2-111">The lower word contains a marshaling context flag as defined by the COM channel.</span></span> <span data-ttu-id="220f2-112">欄位內旗標的確切版面配置會在 [type \_ UserSize](the-type-usersize-function.md)函式中描述。</span><span class="sxs-lookup"><span data-stu-id="220f2-112">The exact layout of the flags within the field is described in [The type\_UserSize Function](the-type-usersize-function.md).</span></span>

<span data-ttu-id="220f2-113">*PMyObj* 參數是使用者類型物件的指標。</span><span class="sxs-lookup"><span data-stu-id="220f2-113">The *pMyObj* parameter is a pointer to a user type object.</span></span> <span data-ttu-id="220f2-114">NDR 引擎會釋放最上層物件。</span><span class="sxs-lookup"><span data-stu-id="220f2-114">The NDR engine frees the top-level object.</span></span> <span data-ttu-id="220f2-115">您必須負責釋放最上層物件可能指向的任何物件。</span><span class="sxs-lookup"><span data-stu-id="220f2-115">You are responsible for freeing any objects to which the top-level object may point.</span></span>

<span data-ttu-id="220f2-116">必須在本機攔截和處理例外狀況，不能允許例外狀況 propigated 呼叫堆疊。</span><span class="sxs-lookup"><span data-stu-id="220f2-116">Exceptions must be caught and handled locally, exceptions must not be allowed to propigated up the call stack.</span></span>

## <a name="related-topics"></a><span data-ttu-id="220f2-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="220f2-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="220f2-118">封送處理使用者 \_ 封送處理和網路封送處理的規則 \_</span><span class="sxs-lookup"><span data-stu-id="220f2-118">Marshaling Rules for user\_marshal and wire\_marshal</span></span>](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[<span data-ttu-id="220f2-119">網路 \_ 封送處理</span><span class="sxs-lookup"><span data-stu-id="220f2-119">wire\_marshal</span></span>](/windows/desktop/Midl/wire-marshal)
</dt> <dt>

[<span data-ttu-id="220f2-120">使用者 \_ 封送處理</span><span class="sxs-lookup"><span data-stu-id="220f2-120">user\_marshal</span></span>](/windows/desktop/Midl/user-marshal)
</dt> </dl>

 

 