---
description: 您可以指定驅動程式裁剪框架。
ms.assetid: a4f53568-684b-48cf-835b-915cefb45a5d
title: 裁剪框架
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1507b82ffedeb26939d5d954f116bb009ed0ab41
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983609"
---
# <a name="clipping-a-frame"></a><span data-ttu-id="b0b24-103">裁剪框架</span><span class="sxs-lookup"><span data-stu-id="b0b24-103">Clipping a Frame</span></span>

<span data-ttu-id="b0b24-104">您可以指定驅動程式裁剪框架。</span><span class="sxs-lookup"><span data-stu-id="b0b24-104">You can specify that the driver clip the frames.</span></span> <span data-ttu-id="b0b24-105"> (如果省略其他 capture 篩選區段，這可能是您的捕獲篩選) 的唯一功能。</span><span class="sxs-lookup"><span data-stu-id="b0b24-105">(If the other capture filter sections are omitted, this may be the only function of your capture filter).</span></span> <span data-ttu-id="b0b24-106">如果 **nFrameBytesToCopy** 欄位不是零 (0) ，其值會指定要保留的每個框架的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="b0b24-106">If the **nFrameBytesToCopy** field is not zero (0), its value specifies how many bytes of each frame received to retain.</span></span> <span data-ttu-id="b0b24-107">如果欄位為零，則會保留整個框架。</span><span class="sxs-lookup"><span data-stu-id="b0b24-107">If the field is zero, then the whole frame is retained.</span></span>

> [!Note]  
> <span data-ttu-id="b0b24-108">您可以藉由設定 **nFrameBytesToCopy** 來裁剪任何通過捕捉篩選器其他部分的畫面格。</span><span class="sxs-lookup"><span data-stu-id="b0b24-108">You may clip any frame that passes the other portions of your capture filter by setting **nFrameBytesToCopy**.</span></span>

 

 

 



