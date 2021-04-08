---
title: OP_POLICY_ELEMENT_LIST
description: OP_POLICY_ELEMENT_LIST IDL 定義
ms.assetid: 1eebbdd2-655b-4bd3-938c-6bc687ffe7bb
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 3c46e7208e6c142b9f58a7704be9bd3461c845b2
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "103684207"
---
# <a name="op_policy_element_list-structure"></a><span data-ttu-id="75ecc-103">OP_POLICY_ELEMENT_LIST 結構</span><span class="sxs-lookup"><span data-stu-id="75ecc-103">OP_POLICY_ELEMENT_LIST structure</span></span>

<span data-ttu-id="75ecc-104">定義根登錄機碼，以及要在該機碼下設定的登錄機碼元素陣列。</span><span class="sxs-lookup"><span data-stu-id="75ecc-104">Defines  a root registry key and an array of registry key elements to be configured under that key.</span></span>

## <a name="syntax"></a><span data-ttu-id="75ecc-105">語法</span><span class="sxs-lookup"><span data-stu-id="75ecc-105">Syntax</span></span>

```C++
typedef struct _OP_POLICY_ELEMENT_LIST
{
    [string] wchar_t                            *pSource;
    ULONG                                       ulRootKeyId;
    ULONG                                       cElements;
    [size_is(cElements)]    POP_POLICY_ELEMENT  pElements;
} OP_POLICY_ELEMENT_LIST, *POP_POLICY_ELEMENT_LIST;
```

## <a name="members"></a><span data-ttu-id="75ecc-106">成員</span><span class="sxs-lookup"><span data-stu-id="75ecc-106">Members</span></span>

### <a name="psource"></a><span data-ttu-id="75ecc-107">pSource</span><span class="sxs-lookup"><span data-stu-id="75ecc-107">pSource</span></span>

<span data-ttu-id="75ecc-108">包含所包含之元素來源群組原則檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="75ecc-108">Contains the path of the Group Policy file that the contained elements were sourced from.</span></span>

### <a name="ulrootkeyid"></a><span data-ttu-id="75ecc-109">ulRootKeyId</span><span class="sxs-lookup"><span data-stu-id="75ecc-109">ulRootKeyId</span></span>

<span data-ttu-id="75ecc-110">包含根登錄機碼的識別碼;目前必須設定為 HKEY_LOCAL_MACHINE。</span><span class="sxs-lookup"><span data-stu-id="75ecc-110">Contains the identifier of the root registry key; currently must be set to HKEY_LOCAL_MACHINE.</span></span>

### <a name="celements"></a><span data-ttu-id="75ecc-111">cElements</span><span class="sxs-lookup"><span data-stu-id="75ecc-111">cElements</span></span>

<span data-ttu-id="75ecc-112">包含 pElements 中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="75ecc-112">Contains the number of elements in pElements.</span></span>

### <a name="pelements"></a><span data-ttu-id="75ecc-113">pElements</span><span class="sxs-lookup"><span data-stu-id="75ecc-113">pElements</span></span>

<span data-ttu-id="75ecc-114">包含 OP_POLICY_ELEMENT 元素的陣列。</span><span class="sxs-lookup"><span data-stu-id="75ecc-114">Contains an array of OP_POLICY_ELEMENT elements.</span></span>

## <a name="see-also"></a><span data-ttu-id="75ecc-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75ecc-115">See also</span></span>

[<span data-ttu-id="75ecc-116">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="75ecc-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)

[<span data-ttu-id="75ecc-117">**OP \_ 原則 \_ 元素**</span><span class="sxs-lookup"><span data-stu-id="75ecc-117">**OP\_POLICY\_ELEMENT**</span></span>](odj-op_policy_element.md)
