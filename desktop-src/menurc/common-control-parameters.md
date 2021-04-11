---
title: 通用控制項參數
description: 以下描述 control 資源定義語句的一般語法。
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261c71163276ed39841d6f6d7e125d4eb5420072
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314914"
---
# <a name="common-control-parameters"></a><span data-ttu-id="f9263-103">通用控制項參數</span><span class="sxs-lookup"><span data-stu-id="f9263-103">Common Control Parameters</span></span>

<span data-ttu-id="f9263-104">以下描述 control 資源定義語句的一般語法。</span><span class="sxs-lookup"><span data-stu-id="f9263-104">The following describes the general syntax for a control resource-definition statement.</span></span> <span data-ttu-id="f9263-105">以下提供每個參數的意義。</span><span class="sxs-lookup"><span data-stu-id="f9263-105">The meaning of each parameter is given below.</span></span> <span data-ttu-id="f9263-106">有時候，語句會以不同的方式使用參數，或可能忽略參數。</span><span class="sxs-lookup"><span data-stu-id="f9263-106">Occasionally, a statement will use a parameter differently, or may ignore a parameter.</span></span> <span data-ttu-id="f9263-107">語句特定的變化會在語句的檔中說明。</span><span class="sxs-lookup"><span data-stu-id="f9263-107">The statement-specific variation is described in the documentation for the statement.</span></span>

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span data-ttu-id="f9263-108"><span id="text"></span><span id="TEXT"></span>*文本*</span><span class="sxs-lookup"><span data-stu-id="f9263-108"><span id="text"></span><span id="TEXT"></span>*text*</span></span>
</dt> <dd>

<span data-ttu-id="f9263-109">要與控制項一起顯示的文字。</span><span class="sxs-lookup"><span data-stu-id="f9263-109">Text that is to be displayed with the control.</span></span> <span data-ttu-id="f9263-110">文字位於控制項內或在控制項旁邊。</span><span class="sxs-lookup"><span data-stu-id="f9263-110">The text is positioned within the control or adjacent to the control.</span></span>

<span data-ttu-id="f9263-111">此參數必須包含以雙引號括住的零或多個字元 ( ") 。</span><span class="sxs-lookup"><span data-stu-id="f9263-111">This parameter must contain zero or more characters enclosed in double quotation marks (").</span></span> <span data-ttu-id="f9263-112">字串會自動以 null 終止，並在產生的資源檔中轉換成 Unicode。</span><span class="sxs-lookup"><span data-stu-id="f9263-112">Strings are automatically null-terminated and converted to Unicode in the resulting resource file.</span></span>

<span data-ttu-id="f9263-113">依預設，雙引號之間列出的字元是 ANSI 字元，而 escape 序列則會被視為位元組 escape 序列。</span><span class="sxs-lookup"><span data-stu-id="f9263-113">By default, the characters listed between the double quotation marks are ANSI characters, and escape sequences are interpreted as byte escape sequences.</span></span> <span data-ttu-id="f9263-114">如果字串前面加上 "L" 前置詞，則字串為寬字元字串，且會將 escape 序列轉譯為指定 Unicode 字元的2位元組轉義順序。</span><span class="sxs-lookup"><span data-stu-id="f9263-114">If the string is preceded by the "L" prefix, the string is a wide-character string and escape sequences are interpreted as 2-byte escape sequences that specify Unicode characters.</span></span> <span data-ttu-id="f9263-115">如果文字中需要雙引號，則必須包含雙引號兩次。</span><span class="sxs-lookup"><span data-stu-id="f9263-115">If a double quotation mark is required in the text, you must include the double quotation mark twice.</span></span>

<span data-ttu-id="f9263-116">文字中的 & 符號 (&) 字元表示會使用下列字元作為控制項的助憶鍵字元。</span><span class="sxs-lookup"><span data-stu-id="f9263-116">An ampersand (&) character in the text indicates that the following character is used as a mnemonic character for the control.</span></span> <span data-ttu-id="f9263-117">當控制項顯示時，不會顯示 & 符號，但是助憶鍵字元會加上底線。</span><span class="sxs-lookup"><span data-stu-id="f9263-117">When the control is displayed, the ampersand is not shown, but the mnemonic character is underlined.</span></span> <span data-ttu-id="f9263-118">使用者可以藉由按下對應到加上底線的助憶鍵字元的按鍵來選擇控制項。</span><span class="sxs-lookup"><span data-stu-id="f9263-118">The user can choose the control by pressing the key corresponding to the underlined mnemonic character.</span></span> <span data-ttu-id="f9263-119">若要使用連字號做為字串中的字元，請 (&&) 插入兩個符號。</span><span class="sxs-lookup"><span data-stu-id="f9263-119">To use the ampersand as a character in a string, insert two ampersands (&&).</span></span>

</dd> <dt>

<span data-ttu-id="f9263-120"><span id="id"></span><span id="ID"></span>*Id*</span><span class="sxs-lookup"><span data-stu-id="f9263-120"><span id="id"></span><span id="ID"></span>*id*</span></span>
</dt> <dd>

<span data-ttu-id="f9263-121">控制識別碼。</span><span class="sxs-lookup"><span data-stu-id="f9263-121">Control identifier.</span></span> <span data-ttu-id="f9263-122">這個值必須是0到65535範圍中的16位不帶正負號的整數，或是評估為該範圍中值的簡單算術運算式。</span><span class="sxs-lookup"><span data-stu-id="f9263-122">This value must be a 16-bit unsigned integer in the range 0 through 65,535 or a simple arithmetic expression that evaluates to a value in that range.</span></span>

</dd> <dt>

<span data-ttu-id="f9263-123"><span id="x"></span><span id="X"></span>*X*</span><span class="sxs-lookup"><span data-stu-id="f9263-123"><span id="x"></span><span id="X"></span>*x*</span></span>
</dt> <dd>

<span data-ttu-id="f9263-124">相對於對話方塊左邊的控制項左邊的 X 座標（X）。</span><span class="sxs-lookup"><span data-stu-id="f9263-124">X-coordinate of the left side of the control relative to the left side of the dialog box.</span></span> <span data-ttu-id="f9263-125">這個值必須是0到65535範圍中的16位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="f9263-125">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="f9263-126">座標是在對話方塊單位中，而且相對於對話方塊、視窗或控制項（包含指定的控制項）的原點。</span><span class="sxs-lookup"><span data-stu-id="f9263-126">The coordinate is in dialog units and is relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="f9263-127"><span id="y"></span><span id="Y"></span>*Y*</span><span class="sxs-lookup"><span data-stu-id="f9263-127"><span id="y"></span><span id="Y"></span>*y*</span></span>
</dt> <dd>

<span data-ttu-id="f9263-128">相對於對話方塊頂端之控制項頂端的 Y 座標。</span><span class="sxs-lookup"><span data-stu-id="f9263-128">Y-coordinate of the top side of the control relative to the top of the dialog box.</span></span> <span data-ttu-id="f9263-129">這個值必須是0到65535範圍中的16位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="f9263-129">This value must be a 16-bit unsigned integer in the range 0 through 65,535.</span></span> <span data-ttu-id="f9263-130">相對於對話方塊、視窗或控制項（包含指定的控制項）的原點，座標是在對話方塊單位中。</span><span class="sxs-lookup"><span data-stu-id="f9263-130">The coordinate is in dialog units relative to the origin of the dialog box, window, or control containing the specified control.</span></span>

</dd> <dt>

<span data-ttu-id="f9263-131"><span id="width"></span><span id="WIDTH"></span>*寬度*</span><span class="sxs-lookup"><span data-stu-id="f9263-131"><span id="width"></span><span id="WIDTH"></span>*width*</span></span>
</dt> <dd>

<span data-ttu-id="f9263-132">控制項的寬度。</span><span class="sxs-lookup"><span data-stu-id="f9263-132">Width of the control.</span></span> <span data-ttu-id="f9263-133">此值必須是介於1到65535之間的16位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="f9263-133">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="f9263-134">寬度為 1/4 個字元的單位。</span><span class="sxs-lookup"><span data-stu-id="f9263-134">The width is in 1/4-character units.</span></span>

</dd> <dt>

<span data-ttu-id="f9263-135"><span id="height"></span><span id="HEIGHT"></span>*高度*</span><span class="sxs-lookup"><span data-stu-id="f9263-135"><span id="height"></span><span id="HEIGHT"></span>*height*</span></span>
</dt> <dd>

<span data-ttu-id="f9263-136">控制項的高度。</span><span class="sxs-lookup"><span data-stu-id="f9263-136">Height of the control.</span></span> <span data-ttu-id="f9263-137">此值必須是介於1到65535之間的16位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="f9263-137">This value must be a 16-bit unsigned integer in the range 1 through 65,535.</span></span> <span data-ttu-id="f9263-138">高度為 1/8 個字元的單位。</span><span class="sxs-lookup"><span data-stu-id="f9263-138">The height is in 1/8-character units.</span></span>

</dd> <dt>

<span data-ttu-id="f9263-139"><span id="style"></span><span id="STYLE"></span>*風格*</span><span class="sxs-lookup"><span data-stu-id="f9263-139"><span id="style"></span><span id="STYLE"></span>*style*</span></span>
</dt> <dd>

<span data-ttu-id="f9263-140">控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="f9263-140">Control styles.</span></span> <span data-ttu-id="f9263-141">使用位 OR (\|) 運算子來合併樣式。</span><span class="sxs-lookup"><span data-stu-id="f9263-141">Use the bitwise OR (\|) operator to combine styles.</span></span> <span data-ttu-id="f9263-142">如需詳細資訊，請參閱 [視窗樣式](../winmsg/window-styles.md)。</span><span class="sxs-lookup"><span data-stu-id="f9263-142">For more information, see [Window Styles](../winmsg/window-styles.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9263-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*擴充樣式*</span><span class="sxs-lookup"><span data-stu-id="f9263-143"><span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*extended-style*</span></span>
</dt> <dd>

<span data-ttu-id="f9263-144">擴充的視窗樣式。</span><span class="sxs-lookup"><span data-stu-id="f9263-144">Extended window styles.</span></span> <span data-ttu-id="f9263-145">您必須指定 *樣式* 以指定 *延伸樣式*。</span><span class="sxs-lookup"><span data-stu-id="f9263-145">You must specify *style* to specify *extended-style*.</span></span> <span data-ttu-id="f9263-146">如需詳細資訊，請參閱 [**EXSTYLE**](exstyle-statement.md)。</span><span class="sxs-lookup"><span data-stu-id="f9263-146">For more information, see [**EXSTYLE**](exstyle-statement.md).</span></span>

</dd> <dt>

<span data-ttu-id="f9263-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*h*</span><span class="sxs-lookup"><span data-stu-id="f9263-147"><span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*</span></span>
</dt> <dd>

<span data-ttu-id="f9263-148">指出在 [**WM \_**](../shell/wm-help.md) 說明處理期間用來識別控制項之識別碼的數值運算式。</span><span class="sxs-lookup"><span data-stu-id="f9263-148">Numeric expression indicating the ID used to identify the control during [**WM\_HELP**](../shell/wm-help.md) processing.</span></span>

</dd> <dt>

<span data-ttu-id="f9263-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span><span class="sxs-lookup"><span data-stu-id="f9263-149"><span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*</span></span>
</dt> <dd>

<span data-ttu-id="f9263-150">控制項的控制項特定資料。</span><span class="sxs-lookup"><span data-stu-id="f9263-150">Control-specific data for the control.</span></span> <span data-ttu-id="f9263-151">當您建立對話方塊，並在該對話方塊中建立具有控制項特定資料的控制項時，該資料的指標會透過該控制項的 [**WM \_ CREATE**](../winmsg/wm-create.md) message *lParam* 傳遞至控制項的視窗程式。</span><span class="sxs-lookup"><span data-stu-id="f9263-151">When a dialog is created, and a control in that dialog which has control-specific data is created, a pointer to that data is passed into the control's window procedure through the *lParam* of the [**WM\_CREATE**](../winmsg/wm-create.md) message for that control.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9263-152">備註</span><span class="sxs-lookup"><span data-stu-id="f9263-152">Remarks</span></span>

<span data-ttu-id="f9263-153">水準對話單位是對話方塊基底寬度單位的1/4。</span><span class="sxs-lookup"><span data-stu-id="f9263-153">Horizontal dialog units are 1/4 of the dialog base width unit.</span></span> <span data-ttu-id="f9263-154">垂直單位是對話方塊基底高度單位的1/8。</span><span class="sxs-lookup"><span data-stu-id="f9263-154">Vertical units are 1/8 of the dialog base height unit.</span></span> <span data-ttu-id="f9263-155">目前的對話方塊基礎單位是從目前系統字型的高度和寬度計算。</span><span class="sxs-lookup"><span data-stu-id="f9263-155">The current dialog base units are computed from the height and width of the current system font.</span></span> <span data-ttu-id="f9263-156">[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)函式會傳回對話方塊基礎單位（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="f9263-156">The [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) function returns the dialog base units in pixels.</span></span> <span data-ttu-id="f9263-157">座標相對於對話方塊的原點。</span><span class="sxs-lookup"><span data-stu-id="f9263-157">The coordinates are relative to the origin of the dialog box.</span></span>

 

 