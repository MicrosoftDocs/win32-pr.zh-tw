---
description: GUID 資料類型是一種文字字串，代表 (識別碼) 的類別識別碼。 COM 必須能夠將字串轉換成有效的類別識別碼。 所有 Guid 都必須以大寫撰寫。
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: 'GUID (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297c9995d537f6cf4b9d2ccf35488e27dc35903f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985206"
---
# <a name="guid"></a><span data-ttu-id="9637c-105">GUID</span><span class="sxs-lookup"><span data-stu-id="9637c-105">GUID</span></span>

<span data-ttu-id="9637c-106">GUID 資料類型是一種文字字串，代表 (識別碼) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="9637c-106">The GUID data type is a text string representing a Class identifier (ID).</span></span> <span data-ttu-id="9637c-107">COM 必須能夠將字串轉換成有效的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="9637c-107">COM must be able to convert the string to a valid Class ID.</span></span> <span data-ttu-id="9637c-108">所有 Guid 都必須以大寫撰寫。</span><span class="sxs-lookup"><span data-stu-id="9637c-108">All GUIDs must be authored in uppercase.</span></span>

<span data-ttu-id="9637c-109">GUID 的有效格式是 {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}，其中 X 是十六進位數位 (0、1、2、3、4、5、6、7、8、9、A、B、C、D、E、F) 。</span><span class="sxs-lookup"><span data-stu-id="9637c-109">The valid format for a GUID is {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} where X is a hex digit (0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F).</span></span>

<span data-ttu-id="9637c-110">請注意，GUIDGEN 之類的公用程式可以產生包含小寫字母的 Guid。</span><span class="sxs-lookup"><span data-stu-id="9637c-110">Note that utilities such as GUIDGEN can generate GUIDs containing lowercase letters.</span></span> <span data-ttu-id="9637c-111">這些必須全部變更為大寫字母，安裝程式才能使用 GUID 做為有效的產品代碼、封裝碼或元件程式碼。</span><span class="sxs-lookup"><span data-stu-id="9637c-111">These must all be changed to uppercase letters before the GUID can be used by the installer as a valid product code, package code, or component code.</span></span>

 

 



