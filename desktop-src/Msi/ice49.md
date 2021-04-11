---
description: ICE49 會檢查不是 REG SZ 型別的預設登錄專案 \_ 。
ms.assetid: 53d976fe-07d2-4b68-ae21-1dbd00d76942
title: ICE49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5edc5ba319380e92fe7d1b7410673c1c688eb337
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851179"
---
# <a name="ice49"></a><span data-ttu-id="91afe-103">ICE49</span><span class="sxs-lookup"><span data-stu-id="91afe-103">ICE49</span></span>

<span data-ttu-id="91afe-104">ICE49 會檢查不是 **REG \_ SZ** 型別的預設登錄專案。</span><span class="sxs-lookup"><span data-stu-id="91afe-104">ICE49 checks for default registry entries that are not a **REG\_SZ** type.</span></span>

## <a name="result"></a><span data-ttu-id="91afe-105">結果</span><span class="sxs-lookup"><span data-stu-id="91afe-105">Result</span></span>

<span data-ttu-id="91afe-106">如果預設登錄專案不是 **REG \_ SZ** 型別，ICE49 會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="91afe-106">ICE49 posts an warning if there is a default registry entry that is not a **REG\_SZ** type.</span></span>

## <a name="example"></a><span data-ttu-id="91afe-107">範例</span><span class="sxs-lookup"><span data-stu-id="91afe-107">Example</span></span>

<span data-ttu-id="91afe-108">ICE49 會針對所顯示的範例報告下列警告。</span><span class="sxs-lookup"><span data-stu-id="91afe-108">ICE49 reports the following warning for the example shown.</span></span>

``` syntax
Reg Entry 'Reg1' is not of type REG_SZ. Default types must be REG_SZ 
    on Win95 Systems. Make sure the component is conditionalized 
    to never be installed on Win95 machines.
```

<span data-ttu-id="91afe-109">值 ' \# 123 ' 是 **DWORD** 登錄值。</span><span class="sxs-lookup"><span data-stu-id="91afe-109">The value '\#123' is a **DWORD** registry value.</span></span>

<span data-ttu-id="91afe-110">登錄[表](registry-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="91afe-110">[Registry Table](registry-table.md) (partial)</span></span>



| <span data-ttu-id="91afe-111">登錄</span><span class="sxs-lookup"><span data-stu-id="91afe-111">Registry</span></span> | <span data-ttu-id="91afe-112">Name</span><span class="sxs-lookup"><span data-stu-id="91afe-112">Name</span></span> | <span data-ttu-id="91afe-113">值</span><span class="sxs-lookup"><span data-stu-id="91afe-113">Value</span></span> |
|----------|------|-------|
| <span data-ttu-id="91afe-114">Reg1</span><span class="sxs-lookup"><span data-stu-id="91afe-114">Reg1</span></span>     |      | <span data-ttu-id="91afe-115">\#123</span><span class="sxs-lookup"><span data-stu-id="91afe-115">\#123</span></span> |



 

<span data-ttu-id="91afe-116">若要修正此警告，請將值變更為輸入 **REG \_ SZ**。</span><span class="sxs-lookup"><span data-stu-id="91afe-116">To fix this warning, change the value to type **REG\_SZ**.</span></span>

<span data-ttu-id="91afe-117">具有非 **REG \_ SZ** 的元件是有效的。</span><span class="sxs-lookup"><span data-stu-id="91afe-117">Components with non-**REG\_SZ** are valid.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91afe-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="91afe-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91afe-119">條件陳述式語法</span><span class="sxs-lookup"><span data-stu-id="91afe-119">Conditional Statement Syntax</span></span>](conditional-statement-syntax.md)
</dt> <dt>

[<span data-ttu-id="91afe-120">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="91afe-120">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



