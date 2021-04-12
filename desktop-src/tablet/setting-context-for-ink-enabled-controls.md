---
description: 啟用筆墨之控制項的所有辨識都會透過 RecognizerCoNtext 物件進行。 Tablet PC 技術 Api 可讓您設定 RecognizerCoNtext 物件上的「模擬」屬性。
ms.assetid: 453993a7-f055-4d84-870c-256d1ec17731
title: 設定 Ink-Enabled 控制項的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6776978834f030353a84c04f03e5ecf05ba060cc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320427"
---
# <a name="setting-context-for-ink-enabled-controls"></a><span data-ttu-id="99d05-104">設定 Ink-Enabled 控制項的內容</span><span class="sxs-lookup"><span data-stu-id="99d05-104">Setting Context for Ink-Enabled Controls</span></span>

<span data-ttu-id="99d05-105">啟用筆墨之控制項的所有辨識都會透過 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件進行。</span><span class="sxs-lookup"><span data-stu-id="99d05-105">All recognition for ink-enabled controls occurs through a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="99d05-106">Tablet PC 技術 Api 可讓您設定 **RecognizerCoNtext** 物件上的「[**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)」屬性。</span><span class="sxs-lookup"><span data-stu-id="99d05-106">The Tablet PC Technology APIs enable you to set the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property on a **RecognizerContext** object.</span></span>

<span data-ttu-id="99d05-107">如果您要建立啟用筆墨的應用程式，請使用 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件的「 [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) 」和「 [**單詞表**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) 」屬性來設定內容。</span><span class="sxs-lookup"><span data-stu-id="99d05-107">If you are creating an ink-enabled application, use the [**RecognizerContext**](inkrecognizercontext-class.md) object's [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) and [**WordList**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist) properties to set contexts.</span></span>

<span data-ttu-id="99d05-108">您可以將 [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) 列舉所定義之輸入範圍中的名稱字串值傳遞給 [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) 程式屬性，並以開啟的 ( 來分隔！</span><span class="sxs-lookup"><span data-stu-id="99d05-108">You may pass in the string values of the names in the input scopes defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration to the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property, delimited with an opening (!</span></span> <span data-ttu-id="99d05-109">和結束 ) 。</span><span class="sxs-lookup"><span data-stu-id="99d05-109">and a closing ).</span></span> <span data-ttu-id="99d05-110">例如，若要將 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件的內容設定為對 URL 中使用的字元進行偏差，請使用下列 C 範例所示的語法 \# ：</span><span class="sxs-lookup"><span data-stu-id="99d05-110">For example, to set the context for a [**RecognizerContext**](inkrecognizercontext-class.md) object to bias toward characters used in a URL, use the syntax shown in the following C\# examples:</span></span>


```C++
theRecoContext.Factoid = "(!IS_URL)";
```



> [!Note]  
> <span data-ttu-id="99d05-111">[**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope)列舉中所定義的輸入範圍會取代舊版 Windows XP Tablet PC Edition SDK 中所提供的 factoids，不過這些 factoids 將繼續運作，以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="99d05-111">The input scopes as defined in the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) enumeration supersede the factoids that were available in previous versions of the Windows XP Tablet PC Edition SDK, although these factoids will continue to work in order to provide backward compatibility.</span></span>

 

<span data-ttu-id="99d05-112">下列 C \# 範例會設定郵遞區號的「 [**模擬**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) 」屬性：</span><span class="sxs-lookup"><span data-stu-id="99d05-112">The following C\# example sets the [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) property for postal codes:</span></span>


```C++
theRecognizerContext.Factoid = "(!IS_ADDRESS_POSTALCODE)";
```



<span data-ttu-id="99d05-113">您可以使用手寫的正則運算式語法來合併輸入範圍。</span><span class="sxs-lookup"><span data-stu-id="99d05-113">You can combine input scopes by using the handwriting regular expression syntax.</span></span> <span data-ttu-id="99d05-114">如需使用正則運算式語法的詳細資訊，請參閱 [使用正則運算式的自訂輸入範圍](custom-input-scopes-with-regular-expressions.md)。</span><span class="sxs-lookup"><span data-stu-id="99d05-114">For more details about using regular expression syntax, see [Custom Input Scopes with Regular Expressions](custom-input-scopes-with-regular-expressions.md).</span></span>

<span data-ttu-id="99d05-115">您可以設定 [**RecognizerCoNtext**](inkrecognizercontext-class.md) 物件上的辨識旗標，以影響辨識器的行為。</span><span class="sxs-lookup"><span data-stu-id="99d05-115">You can set recognition flags on the [**RecognizerContext**](inkrecognizercontext-class.md) object to affect the behavior of the recognizer.</span></span> <span data-ttu-id="99d05-116">其中一個這類旗標是 **RecognizerCoNtext** 的 [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes)列舉中的 **強制** 旗標。</span><span class="sxs-lookup"><span data-stu-id="99d05-116">One such flag is the **Coerce** flag in the [**InkRecognitionModes**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionmodes) enumeration of the **RecognizerContext**.</span></span> <span data-ttu-id="99d05-117">**強制** 辨識旗標會強制辨識器傳回符合所設定之模擬專案定義的結果。</span><span class="sxs-lookup"><span data-stu-id="99d05-117">The **Coerce** flag forces the recognizer to return a result that matches the definition of the factoid that is set.</span></span> <span data-ttu-id="99d05-118">例如，如果您的表單需要使用者輸入數值數量，則設定為 [是]，並將 [ [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) ] 屬性設定為 [**已 \_** **強制**]，可能會很有用。</span><span class="sxs-lookup"><span data-stu-id="99d05-118">For example, if you have a form that requires the user to enter a numerical quantity, it may be useful to set the **IS\_NUMBER** factoid and also set the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**.</span></span> <span data-ttu-id="99d05-119">在該實例中， **強制** 旗標可保證辨識器只會傳回數位。</span><span class="sxs-lookup"><span data-stu-id="99d05-119">In that instance, the **Coerce** flag guarantees that the recognizer returns only numbers.</span></span>

<span data-ttu-id="99d05-120">下列 C \# 範例會將 [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) 屬性設定為 **強制** 轉換：</span><span class="sxs-lookup"><span data-stu-id="99d05-120">The following C\# example sets the [**RecognitionFlags**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_recognitionflags) property to **Coerce**:</span></span>


```C++
theRecognizerContext.RecognitionFlags = RecognitionModes.Coerce;
```



<span data-ttu-id="99d05-121">不過，在決定要設定 **強制** 執行旗標時，請特別小心。</span><span class="sxs-lookup"><span data-stu-id="99d05-121">However, use caution when deciding to set the **Coerce** flag.</span></span> <span data-ttu-id="99d05-122">旗標會強制辨識器僅符合模擬程式的定義。</span><span class="sxs-lookup"><span data-stu-id="99d05-122">The flag forces the recognizer to match only the definition of the factoid.</span></span> <span data-ttu-id="99d05-123">例如，如果您設定的是 \_ 電話 \_ FULLTELEPHONENUMBER 輸入範圍和 **強制** 旗標，辨識器會傳回與的定義完全相符的結果，而 \_ \_ 只有電話 FULLTELEPHONENUMBER 輸入範圍。</span><span class="sxs-lookup"><span data-stu-id="99d05-123">For example, if you set the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag, the recognizer returns results that exactly match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope only.</span></span> <span data-ttu-id="99d05-124">如果使用者使用 \_ \_ FULLTELEPHONENUMBER 輸入範圍和 **強制** 旗標設定來寫入 "911"，辨識器可能會傳回空字串或格式為 (xxx) XXX (的隨機字串，其中 X 是數位) 。</span><span class="sxs-lookup"><span data-stu-id="99d05-124">If a user writes "911" with the IS\_TELEPHONE\_FULLTELEPHONENUMBER input scope and the **Coerce** flag set, the recognizer may return either an empty string or a random string in the format of (XXX) XXX-XXXX (where X is a digit).</span></span> <span data-ttu-id="99d05-125">XXX 的格式與的定義不相符 \_ \_ ，即使是有效的電話號碼也是一樣。</span><span class="sxs-lookup"><span data-stu-id="99d05-125">The format of XXX does not match the definition of the IS\_TELEPHONE\_FULLTELEPHONENUMBER factoid, even though it is a valid phone number.</span></span>

<span data-ttu-id="99d05-126">如需每個輸入範圍的支援格式清單，請參閱 [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) 參考。</span><span class="sxs-lookup"><span data-stu-id="99d05-126">For lists of the supported formats for each input scope, see the [**InputScope**](/windows/win32/api/inputscope/ne-inputscope-inputscope) reference.</span></span>

<span data-ttu-id="99d05-127">若要將欄位傳回給辨識器的預設設定，請將 [模擬] 設定為 [ \_ 預設值]，如下列 C 範例所示 \# ：</span><span class="sxs-lookup"><span data-stu-id="99d05-127">To return a field to the default setting for the recognizer, set the factoid to IS\_DEFAULT , as in the following C\# example:</span></span>


```C++
theRecgonizerContext.Factoid = "(!IS_DEFAULT)";
```



<span data-ttu-id="99d05-128">針對使用 [InkEdit](inkedit-control-reference.md) 控制項的應用程式，藉由指定下列內容來設定控制項的模擬型別：</span><span class="sxs-lookup"><span data-stu-id="99d05-128">For applications that use the [InkEdit](inkedit-control-reference.md) control, set the factoid type for the control by specifying:</span></span>


```C++
InkEdit1.Factoid = "(!IS_INPUTSCOPE)"
```



<span data-ttu-id="99d05-129">其中 `IS_INPUTSCOPE` 是您想要套用之輸入範圍的名稱。</span><span class="sxs-lookup"><span data-stu-id="99d05-129">Where `IS_INPUTSCOPE` is the name of the input scope you want to apply.</span></span>

<span data-ttu-id="99d05-130">[InkEdit](inkedit-control-reference.md)控制項不會公開 [**RecognizerCoNtext**](inkrecognizercontext-class.md)物件。</span><span class="sxs-lookup"><span data-stu-id="99d05-130">The [InkEdit](inkedit-control-reference.md) control does not expose a [**RecognizerContext**](inkrecognizercontext-class.md) object.</span></span> <span data-ttu-id="99d05-131">您仍然可以使用 InkEdit 控制項的 [ [**模擬**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) ] 屬性指派內容，但是無法設定 **WORDMODE** 旗標。</span><span class="sxs-lookup"><span data-stu-id="99d05-131">You can still assign context by using the [**Factoid**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid) property of the InkEdit control, but you cannot set the **WORDMODE** flag.</span></span>

 

 
