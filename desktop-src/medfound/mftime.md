---
description: 定義100毫微秒的單位。
ms.assetid: 9273ff1f-382e-4c58-b571-4852545915b3
title: 'MFTIME (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0e82c99c3c4a42b652c04595d086951c3c1a71a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989866"
---
# <a name="mftime"></a><span data-ttu-id="99493-103">MFTIME</span><span class="sxs-lookup"><span data-stu-id="99493-103">MFTIME</span></span>

<span data-ttu-id="99493-104">定義100毫微秒的單位。</span><span class="sxs-lookup"><span data-stu-id="99493-104">Defines units of 100 nanoseconds.</span></span>


```C++
typedef LONGLONG MFTIME;
```



## <a name="examples"></a><span data-ttu-id="99493-105">範例</span><span class="sxs-lookup"><span data-stu-id="99493-105">Examples</span></span>


```C++
const MFTIME ONE_SECOND = 10000000; // One second.
const LONG   ONE_MSEC = 1000;       // One millisecond

// Convert 100-nanosecond units to milliseconds.

inline LONG MFTimeToMsec(const LONGLONG& time)
{
    return (LONG)(time / (ONE_SECOND / ONE_MSEC));
}
```



## <a name="requirements"></a><span data-ttu-id="99493-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="99493-106">Requirements</span></span>



| <span data-ttu-id="99493-107">需求</span><span class="sxs-lookup"><span data-stu-id="99493-107">Requirement</span></span> | <span data-ttu-id="99493-108">值</span><span class="sxs-lookup"><span data-stu-id="99493-108">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="99493-109">標頭</span><span class="sxs-lookup"><span data-stu-id="99493-109">Header</span></span><br/> | <dl> <span data-ttu-id="99493-110"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="99493-110"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="99493-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="99493-111">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99493-112">媒體基礎資料類型</span><span class="sxs-lookup"><span data-stu-id="99493-112">Media Foundation Datatypes</span></span>](media-foundation-datatypes.md)
</dt> </dl>

 

 




