---
description: ProductLanguage 屬性會指定安裝程式應針對使用者介面中未撰寫至資料庫的任何字串使用的語言。
ms.assetid: 5d798825-c70b-4d5a-b88c-a9db40663f6a
title: ProductLanguage 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3199bd2fcef457b40ad98e52f50c595bc424f9a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993572"
---
# <a name="productlanguage-property"></a><span data-ttu-id="7eb63-103">ProductLanguage 屬性</span><span class="sxs-lookup"><span data-stu-id="7eb63-103">ProductLanguage property</span></span>

<span data-ttu-id="7eb63-104">**ProductLanguage** 屬性會指定安裝程式應針對使用者介面中未撰寫至資料庫的任何字串使用的語言。</span><span class="sxs-lookup"><span data-stu-id="7eb63-104">The **ProductLanguage** property specifies the language the installer should use for any strings in the user interface that are not authored into the database.</span></span> <span data-ttu-id="7eb63-105">這個屬性必須是數位語言識別項 (LANGID) 。</span><span class="sxs-lookup"><span data-stu-id="7eb63-105">This property must be a numeric language identifier (LANGID).</span></span> <span data-ttu-id="7eb63-106">如果轉換變更了資料庫中使用者介面的語言，則也應該變更這個屬性的值，以反映新的語言。</span><span class="sxs-lookup"><span data-stu-id="7eb63-106">If a transform changes the language of the user interface in the database, then it should also change the value of this property to reflect the new language.</span></span>

<span data-ttu-id="7eb63-107">此為必要屬性。</span><span class="sxs-lookup"><span data-stu-id="7eb63-107">This property is REQUIRED.</span></span>

## <a name="remarks"></a><span data-ttu-id="7eb63-108">備註</span><span class="sxs-lookup"><span data-stu-id="7eb63-108">Remarks</span></span>

<span data-ttu-id="7eb63-109">**ProductLanguage** 屬性的值必須是 [[**範本摘要**](template-summary.md)] 屬性中所列的其中一種語言。</span><span class="sxs-lookup"><span data-stu-id="7eb63-109">The value of the **ProductLanguage** property must be one of the languages listed in the [**Template Summary**](template-summary.md) property.</span></span>

<span data-ttu-id="7eb63-110">將封裝編寫為非語言相關時，請將 **ProductLanguage** 屬性設定為0，並使用 MS Shell Dlg 字型作為所有撰寫之對話方塊的文字樣式。</span><span class="sxs-lookup"><span data-stu-id="7eb63-110">When authoring a package as language-neutral, set the **ProductLanguage** property to 0 and use the MS Shell Dlg font as the text style for all authored dialogs.</span></span> <span data-ttu-id="7eb63-111">因為某些字型不支援所有字元集，所以您可以使用這個字型來確定文字已正確顯示在所有當地語系化版本的作業系統上。</span><span class="sxs-lookup"><span data-stu-id="7eb63-111">Because some fonts do not support all the character sets, by using this font you can ensure that the text is correctly displayed on all localized versions of the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="7eb63-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="7eb63-112">Requirements</span></span>



| <span data-ttu-id="7eb63-113">需求</span><span class="sxs-lookup"><span data-stu-id="7eb63-113">Requirement</span></span> | <span data-ttu-id="7eb63-114">值</span><span class="sxs-lookup"><span data-stu-id="7eb63-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7eb63-115">版本</span><span class="sxs-lookup"><span data-stu-id="7eb63-115">Version</span></span><br/> | <span data-ttu-id="7eb63-116">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="7eb63-116">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7eb63-117">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="7eb63-117">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7eb63-118">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="7eb63-118">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7eb63-119">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="7eb63-119">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7eb63-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7eb63-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7eb63-121">屬性</span><span class="sxs-lookup"><span data-stu-id="7eb63-121">Properties</span></span>](properties.md)
</dt> </dl>

 

 




