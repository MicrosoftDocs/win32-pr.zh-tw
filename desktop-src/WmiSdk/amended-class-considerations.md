---
description: 您無法在當地語系化的命名空間中建立修改過之類別的實例。 當地語系化的命名空間中修改過的類別會被視為抽象類別，但它們不包含抽象限定詞。
ms.assetid: a0583153-f5d2-4f4c-ab2e-6ec468e665c7
ms.tgt_platform: multiple
title: 修改過的類別考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f77a2caa315ab4878fe619c13c69bd5d2e1a2610
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195560"
---
# <a name="amended-class-considerations"></a><span data-ttu-id="edf9d-104">修改過的類別考慮</span><span class="sxs-lookup"><span data-stu-id="edf9d-104">Amended Class Considerations</span></span>

<span data-ttu-id="edf9d-105">您無法在當地語系化的命名空間中建立修改過之類別的實例。</span><span class="sxs-lookup"><span data-stu-id="edf9d-105">You cannot create instances of the amended classes in the localized namespace.</span></span> <span data-ttu-id="edf9d-106">當地語系化的命名空間中修改過的類別會被視為抽象類別，但它們不包含 [**抽象**](standard-qualifiers.md) 限定詞。</span><span class="sxs-lookup"><span data-stu-id="edf9d-106">Amended classes in the localized namespace are treated as if they are abstract although they do not contain the [**Abstract**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="edf9d-107">如果您使用 WBEM 旗標從當地語系化的命名空間抓取修改過的類別 \_ \_ \_ ，請使用修改過的限定詞旗標， \_ 並從中產生實例，此實例就會包含修改過之類別的所有修改過的限定詞。</span><span class="sxs-lookup"><span data-stu-id="edf9d-107">If you retrieve an amended class from a localized namespace using the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag and spawn an instance from it, the instance contains all of the amended qualifiers of the amended class.</span></span> <span data-ttu-id="edf9d-108">除非您使用 WBEM 旗標執行 **put** 作業 \_ 使用修改過的 \_ \_ \_ 限定詞旗標，否則您無法將這個新類別儲存在包含基本類別定義的命名空間中。</span><span class="sxs-lookup"><span data-stu-id="edf9d-108">You cannot store this new class in the namespace that contains the basic class definition unless you perform the **put** operation with the WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS flag.</span></span> <span data-ttu-id="edf9d-109">此旗標會指示 WMI 先移除任何修改過的限定詞，再儲存物件。</span><span class="sxs-lookup"><span data-stu-id="edf9d-109">This flag instructs WMI to strip away any amended qualifiers before saving the object.</span></span> <span data-ttu-id="edf9d-110">如果您未指定 WBEM \_ 旗標 \_ \_ ，請使用修改過的 \_ 限定詞， **put** 作業會失敗，並出現 WBEM E 修改過的 \_ \_ \_ 物件錯誤。</span><span class="sxs-lookup"><span data-stu-id="edf9d-110">If you do not specify WBEM\_FLAG\_USE\_AMENDED\_QUALIFIERS, the **put** operation fails with a WBEM\_E\_AMENDED\_OBJECT error.</span></span>

 

 



