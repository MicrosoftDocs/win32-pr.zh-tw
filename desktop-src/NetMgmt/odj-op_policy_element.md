---
title: OP_POLICY_ELEMENT
description: OP_POLICY_ELEMENT IDL 定義
ms.assetid: 69f6e0e7-3f47-4fee-8a4c-df94093dcffa
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: df6fc6852a5efd0a6a2e01a805878ed51bc7c263
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104316906"
---
# <a name="op_policy_element-structure"></a><span data-ttu-id="876a0-103">OP_POLICY_ELEMENT 結構</span><span class="sxs-lookup"><span data-stu-id="876a0-103">OP_POLICY_ELEMENT structure</span></span>

<span data-ttu-id="876a0-104">定義登錄機碼和值名稱、類型，以及應該在該金鑰下設定的值。</span><span class="sxs-lookup"><span data-stu-id="876a0-104">Defines a registry key and a value name, type, and value that should be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="876a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="876a0-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_ELEMENT
{
    [string] wchar_t                *pKeyPath;
    [string] wchar_t                *pValueName;
    ULONG                           ulValueType;
    ULONG                           cbValueData;
    [size_is(cbValueData)]  PBYTE   pValueData;
} OP_POLICY_ELEMENT, *POP_POLICY_ELEMENT;
```

## <a name="members"></a><span data-ttu-id="876a0-106">成員</span><span class="sxs-lookup"><span data-stu-id="876a0-106">Members</span></span>

### <a name="pkeypath"></a><span data-ttu-id="876a0-107">pKeyPath</span><span class="sxs-lookup"><span data-stu-id="876a0-107">pKeyPath</span></span>

<span data-ttu-id="876a0-108">包含登錄機碼的路徑。</span><span class="sxs-lookup"><span data-stu-id="876a0-108">Contains the path of the registry key.</span></span>

### <a name="pvaluename"></a><span data-ttu-id="876a0-109">pValueName</span><span class="sxs-lookup"><span data-stu-id="876a0-109">pValueName</span></span>

<span data-ttu-id="876a0-110">包含登錄值的名稱。</span><span class="sxs-lookup"><span data-stu-id="876a0-110">Contains the name of the registry value.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="876a0-111">ulValueType</span><span class="sxs-lookup"><span data-stu-id="876a0-111">ulValueType</span></span>

<span data-ttu-id="876a0-112">包含登錄 [數值型別](../sysinfo/registry-value-types.md)的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="876a0-112">Contains one of the values from [Registry Value Types](../sysinfo/registry-value-types.md).</span></span>

### <a name="cbvaluedata"></a><span data-ttu-id="876a0-113">cbValueData</span><span class="sxs-lookup"><span data-stu-id="876a0-113">cbValueData</span></span>

<span data-ttu-id="876a0-114">包含 pValueData 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="876a0-114">Contains the size of pValueData in bytes.</span></span>

### <a name="ulvaluetype"></a><span data-ttu-id="876a0-115">ulValueType</span><span class="sxs-lookup"><span data-stu-id="876a0-115">ulValueType</span></span>

<span data-ttu-id="876a0-116">包含登錄值的值。</span><span class="sxs-lookup"><span data-stu-id="876a0-116">Contains the value of the registry value.</span></span>

## <a name="see-also"></a><span data-ttu-id="876a0-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="876a0-117">See also</span></span>

[<span data-ttu-id="876a0-118">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="876a0-118">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)