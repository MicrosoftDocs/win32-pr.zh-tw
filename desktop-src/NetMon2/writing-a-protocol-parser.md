---
description: 本主題包含撰寫通訊協定剖析器的相關資訊，並包含剖析器 DLL 必須執行的匯出函數範例。
ms.assetid: 0be87b33-aab0-4986-8a86-914e0a7b8f2d
title: 撰寫通訊協定剖析器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 338c224dd036df747af6ab805dae273f6ad3f510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513149"
---
# <a name="writing-a-protocol-parser"></a><span data-ttu-id="43d7b-103">撰寫通訊協定剖析器</span><span class="sxs-lookup"><span data-stu-id="43d7b-103">Writing a Protocol Parser</span></span>

<span data-ttu-id="43d7b-104">本主題包含撰寫通訊協定剖析器的相關資訊，並包含剖析器 DLL 必須執行的匯出函數範例。</span><span class="sxs-lookup"><span data-stu-id="43d7b-104">This topic contains information about writing a protocol parser, and includes examples of the export functions that the parser DLL must implement.</span></span>

<span data-ttu-id="43d7b-105">本節包含下列主題。</span><span class="sxs-lookup"><span data-stu-id="43d7b-105">The following topics are included in this section.</span></span>



| <span data-ttu-id="43d7b-106">詞彙</span><span class="sxs-lookup"><span data-stu-id="43d7b-106">Term</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="43d7b-107">描述</span><span class="sxs-lookup"><span data-stu-id="43d7b-107">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43d7b-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[程式設計考慮](programming-considerations.md)</span><span class="sxs-lookup"><span data-stu-id="43d7b-108"><span id="Programming_Considerations"></span><span id="programming_considerations"></span><span id="PROGRAMMING_CONSIDERATIONS"></span>[Programming Considerations](programming-considerations.md)</span></span><br/>                                                   | <span data-ttu-id="43d7b-109">識別可協助您撰寫剖析器 DLL 的基本程式設計秘訣。</span><span class="sxs-lookup"><span data-stu-id="43d7b-109">Identifies the basic programming tips to help you write a parser DLL.</span></span><br/>                                                                                    |
| <span data-ttu-id="43d7b-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[執行剖析器匯出函數](implementing-parser-export-functions.md)</span><span class="sxs-lookup"><span data-stu-id="43d7b-110"><span id="Implementing_Parser_Export_Functions"></span><span id="implementing_parser_export_functions"></span><span id="IMPLEMENTING_PARSER_EXPORT_FUNCTIONS"></span>[Implementing Parser Export Functions](implementing-parser-export-functions.md)</span></span><br/> | <span data-ttu-id="43d7b-111">提供執行匯出函數的範例。</span><span class="sxs-lookup"><span data-stu-id="43d7b-111">Provides examples of implementing export functions.</span></span><br/>                                                                                                      |
| <span data-ttu-id="43d7b-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[格式化顯示的資料](formatting-displayed-data.md)</span><span class="sxs-lookup"><span data-stu-id="43d7b-112"><span id="Formatting_Displayed_Data"></span><span id="formatting_displayed_data"></span><span id="FORMATTING_DISPLAYED_DATA"></span>[Formatting Displayed Data](formatting-displayed-data.md)</span></span><br/>                                                        | <span data-ttu-id="43d7b-113">識別在網路監視器 UI 的詳細資料窗格中所顯示的格式化資料的處理常式。</span><span class="sxs-lookup"><span data-stu-id="43d7b-113">Identifies the process of formatting data that is displayed in the details pane of the Network Monitor UI.</span></span><br/>                                               |
| <span data-ttu-id="43d7b-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[指定追蹤集](specifying-a-follow-set.md)</span><span class="sxs-lookup"><span data-stu-id="43d7b-114"><span id="Specifying_a_Follow_Set"></span><span id="specifying_a_follow_set"></span><span id="SPECIFYING_A_FOLLOW_SET"></span>[Specifying a Follow Set](specifying-a-follow-set.md)</span></span><br/>                                                                  | <span data-ttu-id="43d7b-115">識別指定下一組的程式，並顯示網路監視器如何存取下列剖析器集合，以判斷下一個通訊協定。</span><span class="sxs-lookup"><span data-stu-id="43d7b-115">Identifies the process of specifying a follow set, and shows you how Network Monitor accesses the follow set of a parser to determine the next protocol.</span></span><br/> |
| <span data-ttu-id="43d7b-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[指定遞交集](specifying-a-handoff-set.md)</span><span class="sxs-lookup"><span data-stu-id="43d7b-116"><span id="Specifying_a_Handoff_Set"></span><span id="specifying_a_handoff_set"></span><span id="SPECIFYING_A_HANDOFF_SET"></span>[Specifying a Handoff Set](specifying-a-handoff-set.md)</span></span><br/>                                                             | <span data-ttu-id="43d7b-117">識別指定遞交集的程式，並向您顯示剖析器如何存取其交付集以取得下一個通訊協定的控制碼。</span><span class="sxs-lookup"><span data-stu-id="43d7b-117">Identifies the process of specifying a handoff set, and shows you how the parser accesses its handoff set to get a handle to the next protocol.</span></span><br/>          |



 

 

 




