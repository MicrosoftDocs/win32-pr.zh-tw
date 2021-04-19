---
description: M \_ Dlg 成員變數包含交談視窗的控制碼。 當對話方塊視窗處理 WM INITDIALOG 訊息時，就會初始化這個成員變數 \_ 。
ms.assetid: e10ea37e-064a-4832-abda-57b4fad23168
title: 'CBasePropertyPage：： m_Dlg 成員 (Cprop .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_Dlg
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ca26036bc9b16cc98158643caf91e4a233143e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978692"
---
# <a name="cbasepropertypagem_dlg-member"></a><span data-ttu-id="97656-104">CBasePropertyPage：： m \_ Dlg 成員</span><span class="sxs-lookup"><span data-stu-id="97656-104">CBasePropertyPage::m\_Dlg member</span></span>

<span data-ttu-id="97656-105">`m_Dlg`成員變數包含交談視窗的控制碼。</span><span class="sxs-lookup"><span data-stu-id="97656-105">The `m_Dlg` member variable contains a handle to the dialog window.</span></span> <span data-ttu-id="97656-106">當對話方塊視窗處理 WM INITDIALOG 訊息時，就會初始化這個成員變數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="97656-106">This member variable is initialized when the dialog window processes the WM\_INITDIALOG message.</span></span>

## <a name="syntax"></a><span data-ttu-id="97656-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="97656-107">Syntax</span></span>


```C++
HWND m_Dlg;
```



## <a name="requirements"></a><span data-ttu-id="97656-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="97656-108">Requirements</span></span>



| <span data-ttu-id="97656-109">需求</span><span class="sxs-lookup"><span data-stu-id="97656-109">Requirement</span></span> | <span data-ttu-id="97656-110">值</span><span class="sxs-lookup"><span data-stu-id="97656-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97656-111">標頭</span><span class="sxs-lookup"><span data-stu-id="97656-111">Header</span></span><br/>  | <dl> <span data-ttu-id="97656-112"><dt>Cprop (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="97656-112"><dt>Cprop.h (include Streams.h)</dt></span></span> </dl>                                                                                     |
| <span data-ttu-id="97656-113">程式庫</span><span class="sxs-lookup"><span data-stu-id="97656-113">Library</span></span><br/> | <dl> <span data-ttu-id="97656-114"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="97656-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97656-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97656-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97656-116">**CBasePropertyPage 類別**</span><span class="sxs-lookup"><span data-stu-id="97656-116">**CBasePropertyPage Class**</span></span>](cbasepropertypage.md)
</dt> </dl>

 

 




