---
description: '[字碼頁摘要] 屬性是 ANSI 字碼頁的數值，用於儲存在摘要資訊中的任何字串。'
ms.assetid: eea6cb12-7ec9-4ea4-b2b2-9c812dc4b4d9
title: 字碼頁摘要屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08b83b60bb6aaabadb2ee0dcd201000ea32eccef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977535"
---
# <a name="codepage-summary-property"></a><span data-ttu-id="986d7-103">字碼頁摘要屬性</span><span class="sxs-lookup"><span data-stu-id="986d7-103">Codepage Summary property</span></span>

<span data-ttu-id="986d7-104">[ **字碼頁摘要** ] 屬性是 ANSI 字碼頁的數值，用於儲存在摘要資訊中的任何字串。</span><span class="sxs-lookup"><span data-stu-id="986d7-104">The **Codepage Summary** property is the numeric value of the ANSI code page used for any strings that are stored in the summary information.</span></span> <span data-ttu-id="986d7-105">請注意，這並不是安裝資料庫中字串的相同字碼頁。</span><span class="sxs-lookup"><span data-stu-id="986d7-105">Note that this is not the same code page for strings in the installation database.</span></span> <span data-ttu-id="986d7-106">呼叫 Unicode API 函式時，會使用 **字碼頁摘要** 屬性將摘要資訊中的字串轉譯成 Unicode。</span><span class="sxs-lookup"><span data-stu-id="986d7-106">The **Codepage Summary** property is used to translate the strings in the summary information into Unicode when calling the Unicode API functions.</span></span> <span data-ttu-id="986d7-107">在摘要資訊中設定任何字串屬性之前，必須先設定 **字碼頁的摘要** 屬性。</span><span class="sxs-lookup"><span data-stu-id="986d7-107">The **Codepage Summary** property must be set before any string properties are set in the summary information.</span></span>

## <a name="requirements"></a><span data-ttu-id="986d7-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="986d7-108">Requirements</span></span>



| <span data-ttu-id="986d7-109">需求</span><span class="sxs-lookup"><span data-stu-id="986d7-109">Requirement</span></span> | <span data-ttu-id="986d7-110">值</span><span class="sxs-lookup"><span data-stu-id="986d7-110">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="986d7-111">版本</span><span class="sxs-lookup"><span data-stu-id="986d7-111">Version</span></span><br/> | <span data-ttu-id="986d7-112">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="986d7-112">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="986d7-113">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="986d7-113">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="986d7-114">Windows Server 2003 或 Windows XP 上的 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="986d7-114">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="986d7-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="986d7-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="986d7-116">摘要屬性描述</span><span class="sxs-lookup"><span data-stu-id="986d7-116">Summary Property Descriptions</span></span>](summary-property-descriptions.md)
</dt> </dl>

 

 




