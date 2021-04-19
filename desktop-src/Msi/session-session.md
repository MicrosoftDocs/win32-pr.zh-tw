---
description: 會話物件的屬性（Property）屬性（Property）是讀寫屬性（property），這個屬性（property）（property）（Property）（Property）（Property）是由 Session 物件維護，
ms.assetid: 15ce8264-2573-428c-98d9-690cfaae5144
title: Session. Property 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Property
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 9635d5b9ee093f270e4ee7993f78609d60caa13a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983221"
---
# <a name="sessionproperty-property"></a><span data-ttu-id="cfb74-103">Session. Property 屬性</span><span class="sxs-lookup"><span data-stu-id="cfb74-103">Session.Property property</span></span>

<span data-ttu-id="cfb74-104">[**Session**](session-object.md)物件的 property 屬性（ **property** ）是讀寫屬性（property），這個屬性（property）表示指定之安裝程式屬性的字串值（由記憶體內部屬性工作表中的 **Session** 物件維護），或者，如果前面加上百分比符號 (% ) ，則為目前進程的系統內容變數值。</span><span class="sxs-lookup"><span data-stu-id="cfb74-104">The **Property** property of the [**Session**](session-object.md) object is a read-write property that represents the string value of a named installer property, as maintained by the **Session** object in the in-memory Property table, or, if it is prefixed with a percent sign (%), the value of a system environment variable for the current process.</span></span> <span data-ttu-id="cfb74-105">可能會提供字串或整數值。</span><span class="sxs-lookup"><span data-stu-id="cfb74-105">Either string or integer values may be supplied.</span></span> <span data-ttu-id="cfb74-106">不存在的屬性或環境變數相當於其值為 Null。</span><span class="sxs-lookup"><span data-stu-id="cfb74-106">A non-existent property or environment variable is equivalent to its value being Null.</span></span>

<span data-ttu-id="cfb74-107">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="cfb74-107">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfb74-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfb74-108">Syntax</span></span>


```JScript
propVal = Session.Property
Session.Property = propVal 
```



## <a name="property-value"></a><span data-ttu-id="cfb74-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="cfb74-109">Property value</span></span>

<span data-ttu-id="cfb74-110">需要區分大小寫的屬性名稱，或前面加上百分比符號 (% ) 的環境變數名稱不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="cfb74-110">Required case-sensitive name of a property, or a case-insensitive name of an environment variable prefixed by a percent sign (%).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfb74-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfb74-111">Requirements</span></span>



| <span data-ttu-id="cfb74-112">需求</span><span class="sxs-lookup"><span data-stu-id="cfb74-112">Requirement</span></span> | <span data-ttu-id="cfb74-113">值</span><span class="sxs-lookup"><span data-stu-id="cfb74-113">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfb74-114">版本</span><span class="sxs-lookup"><span data-stu-id="cfb74-114">Version</span></span><br/> | <span data-ttu-id="cfb74-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="cfb74-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cfb74-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="cfb74-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cfb74-117">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cfb74-117">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="cfb74-118">DLL</span><span class="sxs-lookup"><span data-stu-id="cfb74-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="cfb74-119"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfb74-119"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="cfb74-120">IID</span><span class="sxs-lookup"><span data-stu-id="cfb74-120">IID</span></span><br/>     | <span data-ttu-id="cfb74-121">IID \_ >isession 定義為 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="cfb74-121">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




