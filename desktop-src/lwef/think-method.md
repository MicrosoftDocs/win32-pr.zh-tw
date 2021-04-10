---
title: 思考方法
description: 思考方法
ms.assetid: a188dd47-6af1-429d-af0a-69451f6b495e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a896c499e11aeaf50bfe9adc82a8330e61fc693
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842199"
---
# <a name="think-method"></a><span data-ttu-id="96470-103">思考方法</span><span class="sxs-lookup"><span data-stu-id="96470-103">Think Method</span></span>

<span data-ttu-id="96470-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="96470-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="96470-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**</span><span class="sxs-lookup"><span data-stu-id="96470-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="96470-106">在「想像」的文字提示字元中，顯示指定字元的指定文字。</span><span class="sxs-lookup"><span data-stu-id="96470-106">Displays the specified text for the specified character in a "thought" word balloon.</span></span>

</dd> <dt>

<span data-ttu-id="96470-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**</span><span class="sxs-lookup"><span data-stu-id="96470-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="96470-108">\*代理程式 ***。 ( "*** CharacterID \* \* *" 的字元 ) 。考慮* \*  \[ *文字*\]</span><span class="sxs-lookup"><span data-stu-id="96470-108">*agent ***.Characters ("*** CharacterID\*\*\*").Think*\* \[*Text*\]</span></span>



| <span data-ttu-id="96470-109">部分</span><span class="sxs-lookup"><span data-stu-id="96470-109">Part</span></span>   | <span data-ttu-id="96470-110">描述</span><span class="sxs-lookup"><span data-stu-id="96470-110">Description</span></span>                                                       |
|--------|-------------------------------------------------------------------|
| <span data-ttu-id="96470-111">*Text*</span><span class="sxs-lookup"><span data-stu-id="96470-111">*Text*</span></span> | <span data-ttu-id="96470-112">選擇性。</span><span class="sxs-lookup"><span data-stu-id="96470-112">Optional.</span></span> <span data-ttu-id="96470-113">字串，指定字元的考慮輸出。</span><span class="sxs-lookup"><span data-stu-id="96470-113">A string that specifies the character's thought output.</span></span> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="96470-114">備註</span><span class="sxs-lookup"><span data-stu-id="96470-114">Remarks</span></span>

<span data-ttu-id="96470-115">就像「 [**說話**](speak-method.md) 」方法一樣，「 **思考** 」方法是佇列要求，它會在文字氣球中顯示文字，但 **覺得** 單字球形球的外觀不同。</span><span class="sxs-lookup"><span data-stu-id="96470-115">Like the [**Speak**](speak-method.md) method, the **Think** method is a queued request that displays text in a word balloon, except that the **Think** word balloon differs visually.</span></span> <span data-ttu-id="96470-116">此外，氣球只支援書簽語音控制項標記 (**\\ Mrk**) 並忽略其他任何語音控制項標記。</span><span class="sxs-lookup"><span data-stu-id="96470-116">In addition, the balloon supports only the Bookmark speech control tag (**\\Mrk**) and ignores any other speech control tags.</span></span> <span data-ttu-id="96470-117">和 **說話** 不同的是， **思考** 方法不會變更字元的動畫狀態。</span><span class="sxs-lookup"><span data-stu-id="96470-117">Unlike **Speak**, the **Think** method does not change the character's animation state.</span></span>

<span data-ttu-id="96470-118">[**球形球**](/windows/desktop/lwef/the-balloon-object)物件的屬性會影響 [**說**](speak-method.md)和 **思考** 方法的輸出。</span><span class="sxs-lookup"><span data-stu-id="96470-118">The [**Balloon**](/windows/desktop/lwef/the-balloon-object) object's properties affect the output of both the [**Speak**](speak-method.md) and **Think** methods.</span></span> <span data-ttu-id="96470-119">例如， **氣球** 物件的 [**Enabled**](enabled-property.md) 屬性必須為 **True** ，才會顯示文字。</span><span class="sxs-lookup"><span data-stu-id="96470-119">For example, the **Balloon** object's [**Enabled**](enabled-property.md) property must be **True** for text to display.</span></span>

<span data-ttu-id="96470-120">如果您宣告物件參考，並將它設定為此方法，則會傳回 [**Request**](/windows/desktop/lwef/the-request-object) 物件。</span><span class="sxs-lookup"><span data-stu-id="96470-120">If you declare an object reference and set it to this method, it returns a [**Request**](/windows/desktop/lwef/the-request-object) object.</span></span> <span data-ttu-id="96470-121">此外，如果檔案尚未載入，伺服器會將 **要求** 物件的 [ [**狀態**](status-property.md) ] 屬性設定為 [失敗]，並提供適當的錯誤碼編號。</span><span class="sxs-lookup"><span data-stu-id="96470-121">In addition, if the file has not been loaded, the server sets the **Request** object's [**Status**](status-property.md) property to "failed" with an appropriate error code number.</span></span>

<span data-ttu-id="96470-122">代理程式自動斷詞字提示字元會中斷使用空白字元的單字 (例如，空格鍵或 Tab) 。</span><span class="sxs-lookup"><span data-stu-id="96470-122">Agent's automatic word breaking in the word balloon breaks words using white-space characters (for example, Space or Tab).</span></span> <span data-ttu-id="96470-123">但是，如果無法使用，它可能會中斷文字以符合氣球。</span><span class="sxs-lookup"><span data-stu-id="96470-123">However, if it cannot, it may break a word to fit the balloon.</span></span> <span data-ttu-id="96470-124">在日文、中文和泰文之類的語言中，不會使用空格來分隔單字，)  (在字元之間插入 Unicode 零寬度空白字元，以定義邏輯字組分隔。</span><span class="sxs-lookup"><span data-stu-id="96470-124">In languages like Japanese, Chinese, and Thai where spaces are not used to break words, insert a Unicode zero-width space character (0x200B) between characters to define logical word breaks.</span></span>

> [!Note]  
> <span data-ttu-id="96470-125">使用「 [**朗讀**](speak-method.md) 」方法之前，請先設定字元的語言識別項，以確保在文字批註內顯示適當的文字。</span><span class="sxs-lookup"><span data-stu-id="96470-125">Set the character's language ID before using the [**Speak**](speak-method.md) method to ensure appropriate text display within the word balloon.</span></span>

 

 

 