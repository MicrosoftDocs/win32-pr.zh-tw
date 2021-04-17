---
description: 網路監視器的框架檢視器會以三個窗格顯示剖析的資料。
ms.assetid: 72770b6f-1cec-4fa4-a91e-85367d531c7f
title: 查看剖析的資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e0d1e82503d8ad78757e7c6cb1b8f02df8bc163
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104555603"
---
# <a name="viewing-parsed-information"></a><span data-ttu-id="dbc3a-103">查看剖析的資訊</span><span class="sxs-lookup"><span data-stu-id="dbc3a-103">Viewing Parsed Information</span></span>

<span data-ttu-id="dbc3a-104">網路監視器的框架檢視器會以三個窗格顯示剖析的資料。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-104">The Network Monitor frame viewer displays parsed data in three panes.</span></span> <span data-ttu-id="dbc3a-105">上方窗格會顯示包含已識別之通訊協定的框架摘要。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-105">The upper pane displays a summary of the frame that includes the identified protocol.</span></span> <span data-ttu-id="dbc3a-106">中間的窗格會顯示格式化的資料屬性，這些屬性可以在剖析器顯示中以階層方式組織。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-106">The middle pane displays the formatted data properties that can be organized hierarchically as part of the parser display.</span></span> <span data-ttu-id="dbc3a-107">下方的窗格會顯示從中間窗格選取的反白顯示原始資料。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-107">The lower pane displays highlighted raw data that is selected from the middle pane.</span></span>

<span data-ttu-id="dbc3a-108">您可以指定當您開發自己的剖析器時，如何顯示檢視器中的資訊。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-108">You can specify how the information in the viewer is displayed when you develop your own parser.</span></span> <span data-ttu-id="dbc3a-109">下圖顯示如何在網路監視器框架檢視器中顯示資訊。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-109">The following illustration shows how information can be displayed in the Network Monitor frame viewer.</span></span>

![網路監視器框架檢視器](images/parseui.png)

> [!Note]  
> <span data-ttu-id="dbc3a-111">剖析器不會顯示畫面格。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-111">Parsers do not display frames.</span></span> <span data-ttu-id="dbc3a-112">剖析器會辨識所提供資訊中的欄位，然後通知網路監視器顯示畫面格。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-112">Parsers recognize fields in the information provided, and then notify Network Monitor to display the frame.</span></span> <span data-ttu-id="dbc3a-113">篩選是較高層級的作業，可讓篩選查詢跨越剖析器。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-113">Filtering is a higher level operation that allows filter queries to span parsers.</span></span>

 

<span data-ttu-id="dbc3a-114">在您的剖析器中，請只使用可在 Microsoft Win32 應用程式上執行的函式。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-114">In your parser, use only functions that can run on Microsoft Win32 applications.</span></span> <span data-ttu-id="dbc3a-115">將屬性附加至原始資料之前，剖析器必須先向網路監視器核心註冊所有可能的屬性。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-115">Before attaching properties to the raw data, a parser must first register all possible properties with the Network Monitor kernel.</span></span> <span data-ttu-id="dbc3a-116">剖析器會將訊息傳送至核心以建立屬性資料庫，然後使用其通訊協定的每個可能屬性來填滿屬性資料庫。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-116">The parser sends a message to the kernel to create a property database, and then fills the property database with every possible property for its protocol.</span></span> <span data-ttu-id="dbc3a-117">屬性資料庫中的每個屬性都包含資訊，例如文字描述、用來格式化原始資料的資料類型和辨識符號，以及用來顯示資料的格式化常式。</span><span class="sxs-lookup"><span data-stu-id="dbc3a-117">Each property in the property database contains information such as a textual description, a data type and qualifier that are used to format the raw data, and a formatting routine that is used to display the data.</span></span>

 

 



