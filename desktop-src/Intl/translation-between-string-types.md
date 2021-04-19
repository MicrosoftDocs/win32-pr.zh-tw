---
description: 下表所列的函式會將字元字串從某個字串類型轉譯成另一個字串類型。
ms.assetid: 26802339-6291-4767-b468-68a9e8e95774
title: 字串類型之間的轉譯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 877721f2d8ce3852011786e487598e3fd068c9eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106974298"
---
# <a name="translation-between-string-types"></a><span data-ttu-id="b6791-103">字串類型之間的轉譯</span><span class="sxs-lookup"><span data-stu-id="b6791-103">Translation Between String Types</span></span>

<span data-ttu-id="b6791-104">下表所列的函式會將字元字串從某個字串類型轉譯成另一個字串類型。</span><span class="sxs-lookup"><span data-stu-id="b6791-104">The functions listed in the following table translate character strings from one string type to another.</span></span>



| <span data-ttu-id="b6791-105">函式</span><span class="sxs-lookup"><span data-stu-id="b6791-105">Function</span></span>                                           | <span data-ttu-id="b6791-106">描述</span><span class="sxs-lookup"><span data-stu-id="b6791-106">Description</span></span>                                             |
|----------------------------------------------------|---------------------------------------------------------|
| [<span data-ttu-id="b6791-107">**FoldString**</span><span class="sxs-lookup"><span data-stu-id="b6791-107">**FoldString**</span></span>](/windows/win32/api/stringapiset/nf-stringapiset-foldstringw)                   | <span data-ttu-id="b6791-108">將一個字元字串轉譯為另一個字元字串。</span><span class="sxs-lookup"><span data-stu-id="b6791-108">Translates one character string to another.</span></span>             |
| [<span data-ttu-id="b6791-109">**LCMapString**</span><span class="sxs-lookup"><span data-stu-id="b6791-109">**LCMapString**</span></span>](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)                 | <span data-ttu-id="b6791-110">依地區設定對應字元字串。</span><span class="sxs-lookup"><span data-stu-id="b6791-110">Maps a character string by locale.</span></span>                      |
| [<span data-ttu-id="b6791-111">**ToUnicode**</span><span class="sxs-lookup"><span data-stu-id="b6791-111">**ToUnicode**</span></span>](/windows/win32/api/winuser/nf-winuser-tounicode)              | <span data-ttu-id="b6791-112">將虛擬按鍵程式碼轉譯為 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="b6791-112">Translates a virtual key code into a Unicode character.</span></span> |
| [<span data-ttu-id="b6791-113">**MultiByteToWideChar**</span><span class="sxs-lookup"><span data-stu-id="b6791-113">**MultiByteToWideChar**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) | <span data-ttu-id="b6791-114">將多位元組字元串對應至 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="b6791-114">Maps a multibyte string to a Unicode string.</span></span>            |
| [<span data-ttu-id="b6791-115">**WideCharToMultiByte**</span><span class="sxs-lookup"><span data-stu-id="b6791-115">**WideCharToMultiByte**</span></span>](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) | <span data-ttu-id="b6791-116">將 Unicode 字串對應到多位元組字元串。</span><span class="sxs-lookup"><span data-stu-id="b6791-116">Maps a Unicode string to a multibyte string.</span></span>            |



 

<span data-ttu-id="b6791-117">[**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)和 [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)函數特別適用于支援數個字串類型的應用程式。</span><span class="sxs-lookup"><span data-stu-id="b6791-117">The [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) and [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) functions are particularly useful for applications that support several string types.</span></span> <span data-ttu-id="b6791-118">ANSI C 也定義了 **wcstombs** 和 **mbstowcs** 的轉換函式，但是只能在標準 C 程式庫所支援的字元集之間進行轉換。</span><span class="sxs-lookup"><span data-stu-id="b6791-118">ANSI C also defines the conversion functions **wcstombs** and **mbstowcs**, but they can only convert to and from the character set supported by the standard C library.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b6791-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="b6791-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b6791-120">Windows API 中的 Unicode</span><span class="sxs-lookup"><span data-stu-id="b6791-120">Unicode in the Windows API</span></span>](unicode-in-the-windows-api.md)
</dt> </dl>

 

 
