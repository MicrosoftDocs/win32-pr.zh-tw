---
title: IDL 檔案
description: IDL 檔案
ms.assetid: 94a6752d-fcf3-47ce-ac3f-be1d1c9768e6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bc9a736bf9b9a77ec1cb655fb5c76e9e1c0d27e
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842780"
---
# <a name="idl-files"></a><span data-ttu-id="9579b-103">IDL 檔案</span><span class="sxs-lookup"><span data-stu-id="9579b-103">IDL Files</span></span>

<span data-ttu-id="9579b-104">COM 使用 Microsoft 介面定義語言 (MIDL) 來描述 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="9579b-104">COM uses the Microsoft Interface Definition Language (MIDL) to describe COM objects.</span></span> <span data-ttu-id="9579b-105">MIDL 是開放式 Software Foundation 所定義之分散式運算環境的 IDL 延伸模組，其開發目的是要針對傳統用戶端/伺服器應用程式中的遠端程序呼叫定義介面。</span><span class="sxs-lookup"><span data-stu-id="9579b-105">MIDL is an extension of the IDL for distributed computing environments defined by the Open Software Foundation, which was developed to define interfaces for remote procedure calls in traditional client/server applications.</span></span> <span data-ttu-id="9579b-106">MIDL 包含物件定義語言的大部分屬性和語句 (ODL) ，這是原本用來產生 OLE Automation 型別程式庫的語言。</span><span class="sxs-lookup"><span data-stu-id="9579b-106">MIDL includes most of the attributes and statements of Object Definition Language (ODL), the language originally used to generate type libraries for OLE Automation.</span></span>

<span data-ttu-id="9579b-107">在 c + + 和 JAVA 中，建立 COM 物件的開發人員會建立一個 IDL 檔案，MIDL 編譯器接著會處理該檔案，以建立類型程式庫或標頭和 proxy 檔案，或兩者。</span><span class="sxs-lookup"><span data-stu-id="9579b-107">In C++ and Java, a developer building a COM object creates an IDL file that the MIDL compiler then processes to create a type library or header and proxy files, or both.</span></span> <span data-ttu-id="9579b-108">*類型程式庫* 是描述 com 物件或 com 介面的二進位檔案，或兩者。</span><span class="sxs-lookup"><span data-stu-id="9579b-108">A *type library* is a binary file that describes the COM object or COM interfaces, or both.</span></span> <span data-ttu-id="9579b-109">類型程式庫是 IDL 檔案的編譯版本。</span><span class="sxs-lookup"><span data-stu-id="9579b-109">A type library is the compiled version of the IDL file.</span></span> <span data-ttu-id="9579b-110">不過，類型程式庫只支援 ODL 語義。</span><span class="sxs-lookup"><span data-stu-id="9579b-110">However, type libraries support ODL semantics only.</span></span> <span data-ttu-id="9579b-111">尤其是，它們無法表示與 IDL 屬性相關的 IDL 檔案中的所有資訊，例如 \[ [**大小 \_**](/windows/desktop/Midl/size-is) \] 。</span><span class="sxs-lookup"><span data-stu-id="9579b-111">In particular, they cannot represent all the information from an IDL file related to IDL attributes like \[[**size\_is**](/windows/desktop/Midl/size-is)\].</span></span> <span data-ttu-id="9579b-112">您必須針對在類型程式庫中遺失資訊的 IDL 檔案，建立和使用 proxy 檔案。</span><span class="sxs-lookup"><span data-stu-id="9579b-112">You need to create and use proxy files for IDL files affected by information loss in the type library.</span></span>

<span data-ttu-id="9579b-113">在 Visual Basic 中，建立 COM 物件的開發人員不會建立 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="9579b-113">In Visual Basic, a developer creating a COM object does not create an IDL file.</span></span> <span data-ttu-id="9579b-114">相反地，Visual Basic 會使用類別和專案屬性來收集資訊，並直接建立類型程式庫。</span><span class="sxs-lookup"><span data-stu-id="9579b-114">Instead, Visual Basic gathers information using class and project properties and directly creates the type library.</span></span>

 

 