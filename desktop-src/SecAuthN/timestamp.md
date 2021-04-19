---
description: TimeStamp 資料類型保存安全性權杖的時間有效性的相關資訊。 TimeStamp 資料類型值的格式與 FILETIME 結構的值相同。
ms.assetid: 0a609b32-dbd7-4905-8990-65ebabcd0668
title: 'TimeStamp (Sspi. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4898e85b0c11f55e5bb0dba2dbdefe2a3b6a2e4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978901"
---
# <a name="timestamp"></a><span data-ttu-id="9c01a-104">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="9c01a-104">TimeStamp</span></span>

<span data-ttu-id="9c01a-105">**TimeStamp** 資料類型保存安全性權杖的時間有效性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9c01a-105">The **TimeStamp** data type holds information about the time validity of security tokens.</span></span> <span data-ttu-id="9c01a-106">**TimeStamp** 資料類型值的格式與 [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime)結構的值相同。</span><span class="sxs-lookup"><span data-stu-id="9c01a-106">The format of the value of the **TimeStamp** data type is the same as that of the [**FILETIME**](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure.</span></span>


```C++
typedef SECURITY_INTEGER TimeStamp, *PTimeStamp;
```



## <a name="requirements"></a><span data-ttu-id="9c01a-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c01a-107">Requirements</span></span>



| <span data-ttu-id="9c01a-108">需求</span><span class="sxs-lookup"><span data-stu-id="9c01a-108">Requirement</span></span> | <span data-ttu-id="9c01a-109">值</span><span class="sxs-lookup"><span data-stu-id="9c01a-109">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c01a-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c01a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="9c01a-111">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c01a-111">Windows XP \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="9c01a-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c01a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="9c01a-113">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9c01a-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                   |
| <span data-ttu-id="9c01a-114">標頭</span><span class="sxs-lookup"><span data-stu-id="9c01a-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="9c01a-115"><dt>Sspi (包含 Security .h) </dt></span><span class="sxs-lookup"><span data-stu-id="9c01a-115"><dt>Sspi.h (include Security.h)</dt></span></span> </dl> |



 

 
