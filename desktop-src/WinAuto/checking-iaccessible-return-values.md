---
title: 檢查 IAccessible 傳回值
description: 用戶端開發人員不應該相依元件物件模型 (COM) 宏成功，而且無法測試 IAccessible 傳回值，因為 S 以外的值 \_ 會被視為成功。
ms.assetid: 0def0349-178b-4be5-aa1d-6602dc015981
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9328c89b0ab2b86e35cf06e74f05dd4937999be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106969919"
---
# <a name="checking-iaccessible-return-values"></a><span data-ttu-id="d3538-103">檢查 IAccessible 傳回值</span><span class="sxs-lookup"><span data-stu-id="d3538-103">Checking IAccessible Return Values</span></span>

<span data-ttu-id="d3538-104">用戶端開發人員不應該相依元件物件模型 (COM) 宏 [**成功**](/windows/desktop/api/winerror/nf-winerror-succeeded) ，而且 [**無法**](/windows/desktop/api/winerror/nf-winerror-failed) 測試 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 傳回值，因為 S 以外的值 \_ 會被視為成功。</span><span class="sxs-lookup"><span data-stu-id="d3538-104">Client developers should not rely on the Component Object Model (COM) macros [**SUCCEEDED**](/windows/desktop/api/winerror/nf-winerror-succeeded) and [**FAILED**](/windows/desktop/api/winerror/nf-winerror-failed) to test [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) return values, because values other than S\_OK are considered a success.</span></span> <span data-ttu-id="d3538-105">例如，方法可以傳回 \_ FALSE，它會被 **成功** 的宏視為成功，但仍會在輸出參數中收到 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="d3538-105">For example, a method can return S\_FALSE, which is considered a success by the **SUCCEEDED** macro, but still receive a **NULL** pointer in an output parameter.</span></span>

<span data-ttu-id="d3538-106">用戶端開發人員必須預防某些伺服器傳回錯誤碼以外的錯誤代碼，而不是記錄的值。</span><span class="sxs-lookup"><span data-stu-id="d3538-106">Client developers must guard against the possibility that some servers return error codes other than the documented values.</span></span> <span data-ttu-id="d3538-107">為了安全起見，您必須確定所有輸出參數都包含有效的資訊並符合下列準則：</span><span class="sxs-lookup"><span data-stu-id="d3538-107">To be safe, you must ensure that all the output parameters contain valid information and meet the following criteria:</span></span>

-   <span data-ttu-id="d3538-108">所有指標皆為非 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d3538-108">All pointers are non-**NULL**.</span></span>
-   <span data-ttu-id="d3538-109">任何 [變異](/windows/win32/api/oaidl/ns-oaidl-variant)結構的 **vt** 成員都不等於 vt \_ 空白。</span><span class="sxs-lookup"><span data-stu-id="d3538-109">The **vt** member of any [VARIANT](/windows/win32/api/oaidl/ns-oaidl-variant) structure is not equal to VT\_EMPTY.</span></span>

 

 