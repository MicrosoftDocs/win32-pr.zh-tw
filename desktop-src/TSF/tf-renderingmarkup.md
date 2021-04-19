---
title: TF_RENDERINGMARKUP 結構
description: TF \_ RENDERINGMARKUP 結構結構包含範圍和顯示內容資訊。
ms.assetid: 206e679b-f2eb-4f28-ac2a-58f3c222a020
keywords:
- TF_RENDERINGMARKUP 結構文字服務架構
topic_type:
- apiref
api_name:
- TF_RENDERINGMARKUP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 166a60182ae7b53dbc70993a7bae81991e42255b
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106968262"
---
# <a name="tf_renderingmarkup-structure"></a><span data-ttu-id="b9cc4-104">TF \_ RENDERINGMARKUP 結構</span><span class="sxs-lookup"><span data-stu-id="b9cc4-104">TF\_RENDERINGMARKUP structure</span></span>

<span data-ttu-id="b9cc4-105">[**TF \_ RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color)結構結構包含範圍和顯示內容資訊。</span><span class="sxs-lookup"><span data-stu-id="b9cc4-105">The [**TF\_RENDERINGMARKUP**](/windows/desktop/api/Msctf/ns-msctf-tf_da_color) structure structure contains a range and the display attribute information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9cc4-106">語法</span><span class="sxs-lookup"><span data-stu-id="b9cc4-106">Syntax</span></span>


```C++
typedef struct {
  ITfRange*           pRange;
  TF_DISPLAYATTRIBUTE tfDisplayAttr;
} TF_RENDERINGMARKUP;
```



## <a name="members"></a><span data-ttu-id="b9cc4-107">成員</span><span class="sxs-lookup"><span data-stu-id="b9cc4-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="b9cc4-108">**pRange**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-108">**pRange**</span></span>
</dt> <dd>

<span data-ttu-id="b9cc4-109">[ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="b9cc4-109">A pointer to an [ITfRange](/windows/desktop/api/Msctf/nn-msctf-itfrange) interface.</span></span>

</dd> <dt>

<span data-ttu-id="b9cc4-110">**tfDisplayAttr**</span><span class="sxs-lookup"><span data-stu-id="b9cc4-110">**tfDisplayAttr**</span></span>
</dt> <dd>

<span data-ttu-id="b9cc4-111">顯示內容資訊。</span><span class="sxs-lookup"><span data-stu-id="b9cc4-111">Display attribute information.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9cc4-112">備註</span><span class="sxs-lookup"><span data-stu-id="b9cc4-112">Remarks</span></span>

<span data-ttu-id="b9cc4-113">此結構目前不在公用標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="b9cc4-113">This structure is not currently in the public header files.</span></span> <span data-ttu-id="b9cc4-114">若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。</span><span class="sxs-lookup"><span data-stu-id="b9cc4-114">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 




