---
title: WMDM_FIND_SCOPE 列舉
description: WMDM \_ 尋找 \_ 範圍列舉型別會定義儲存物件的範圍。
ms.assetid: 971f84d5-8383-4b38-a201-b21100b2f37e
keywords:
- WMDM_FIND_SCOPE 列舉 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_FIND_SCOPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6b65489d14a4f1100b1da33238669310a2731f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999112"
---
# <a name="wmdm_find_scope-enumeration"></a><span data-ttu-id="50732-104">WMDM \_ 尋找 \_ 範圍列舉</span><span class="sxs-lookup"><span data-stu-id="50732-104">WMDM\_FIND\_SCOPE enumeration</span></span>

<span data-ttu-id="50732-105">**WMDM \_ 尋找 \_ 範圍** 列舉型別會定義儲存物件的範圍。</span><span class="sxs-lookup"><span data-stu-id="50732-105">The **WMDM\_FIND\_SCOPE** enumeration type defines the scope of the storage object.</span></span>

## <a name="syntax"></a><span data-ttu-id="50732-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="50732-106">Syntax</span></span>


```C++
typedef enum tagWMDM_FIND_SCOPE { 
  WMDM_FIND_SCOPE_GLOBAL,
  WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN
} WMDM_FIND_SCOPE;
```



## <a name="constants"></a><span data-ttu-id="50732-107">常數</span><span class="sxs-lookup"><span data-stu-id="50732-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="50732-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM \_ 尋找 \_ 範圍 \_ 全域**</span><span class="sxs-lookup"><span data-stu-id="50732-108"><span id="WMDM_FIND_SCOPE_GLOBAL"></span><span id="wmdm_find_scope_global"></span>**WMDM\_FIND\_SCOPE\_GLOBAL**</span></span>
</dt> <dd>

<span data-ttu-id="50732-109">在裝置上的任何位置尋找相符的物件。</span><span class="sxs-lookup"><span data-stu-id="50732-109">Looking for the matching object anywhere on the device.</span></span>

</dd> <dt>

<span data-ttu-id="50732-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM \_ 尋找 \_ 領域 \_ 直屬 \_ 子系**</span><span class="sxs-lookup"><span data-stu-id="50732-110"><span id="WMDM_FIND_SCOPE_IMMEDIATE_CHILDREN"></span><span id="wmdm_find_scope_immediate_children"></span>**WMDM\_FIND\_SCOPE\_IMMEDIATE\_CHILDREN**</span></span>
</dt> <dd>

<span data-ttu-id="50732-111">尋找此儲存體及其子系內相符的物件。</span><span class="sxs-lookup"><span data-stu-id="50732-111">Looking for the matching object within this storage and its children.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="50732-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="50732-112">Requirements</span></span>



| <span data-ttu-id="50732-113">需求</span><span class="sxs-lookup"><span data-stu-id="50732-113">Requirement</span></span> | <span data-ttu-id="50732-114">值</span><span class="sxs-lookup"><span data-stu-id="50732-114">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="50732-115">標頭</span><span class="sxs-lookup"><span data-stu-id="50732-115">Header</span></span><br/> | <dl> <span data-ttu-id="50732-116"><dt>Wmdm .idl</dt></span><span class="sxs-lookup"><span data-stu-id="50732-116"><dt>Wmdm.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="50732-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="50732-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="50732-118">**列舉類型**</span><span class="sxs-lookup"><span data-stu-id="50732-118">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





