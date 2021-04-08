---
title: 程式設計語言支援
description: 您可以撰寫許多語言的 ADSI 用戶端應用程式。
ms.assetid: 47460d57-936d-4c5f-8ff6-a4d9d60d0b68
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4946f05806a6e24ff466d08dc141aadf9c995e5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839148"
---
# <a name="programming-language-support"></a><span data-ttu-id="eaf73-103">程式設計語言支援</span><span class="sxs-lookup"><span data-stu-id="eaf73-103">Programming Language Support</span></span>

<span data-ttu-id="eaf73-104">您可以撰寫許多語言的 ADSI 用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="eaf73-104">You can write ADSI client applications in many languages.</span></span> <span data-ttu-id="eaf73-105">針對大部分的系統管理工作，ADSI 會定義可從符合自動化的語言存取的介面和物件。</span><span class="sxs-lookup"><span data-stu-id="eaf73-105">For the majority of administrative tasks, ADSI defines interfaces and objects accessible from languages compliant with Automation.</span></span> <span data-ttu-id="eaf73-106">例如，Microsoft Visual Basic 開發系統、Microsoft Visual Basic Scripting Edition (VBScript) 和 JAVA，以及更多效能和效率的語言，例如 C 和 c + +。</span><span class="sxs-lookup"><span data-stu-id="eaf73-106">For example, the Microsoft Visual Basic development system, Microsoft Visual Basic Scripting Edition (VBScript), and Java, as well as more performance and efficiency-conscious languages such as C and C++.</span></span>

<span data-ttu-id="eaf73-107">與 Active Server Pages 和 VBScript 的流暢整合，可讓您輕鬆地撰寫可存取目錄服務的網際網路應用程式。</span><span class="sxs-lookup"><span data-stu-id="eaf73-107">Smooth integration with Active Server Pages and VBScript make it easy to write Internet applications that access directory services.</span></span> <span data-ttu-id="eaf73-108">為了與 OLE DB 的應用程式整合，ADSI 藉由支援 OLE DB 查詢介面的子集來提供 OLE DB 提供者。</span><span class="sxs-lookup"><span data-stu-id="eaf73-108">For integration with OLE DB applications, ADSI supplies an OLE DB provider by supporting a subset of the OLE DB query interfaces.</span></span> <span data-ttu-id="eaf73-109">OLE DB 提供者支援 Active Directory 的唯讀存取。</span><span class="sxs-lookup"><span data-stu-id="eaf73-109">The OLE DB provider supports read-only access to Active Directory.</span></span>

<span data-ttu-id="eaf73-110">針對網際網路應用程式，使用 [Active Server 中的腳本] 頁面 (ASP) 檔案可以在伺服器上建立及操作 ADSI 物件，並在網頁中顯示結果。</span><span class="sxs-lookup"><span data-stu-id="eaf73-110">For Internet applications, using scripting in Active Server Page (ASP) files can create and manipulate ADSI objects on the server and display the results in a webpage.</span></span> <span data-ttu-id="eaf73-111">在 Microsoft Management Console 中，目錄-服務管理嵌入式管理單元可以使用 ADSI 來尋找感興趣的目錄服務。</span><span class="sxs-lookup"><span data-stu-id="eaf73-111">In Microsoft Management Console, directory-service administration snap-ins can use ADSI to find directory services of interest.</span></span> <span data-ttu-id="eaf73-112">簡單地說，Active Directory 服務介面可以存取廣泛且多樣化的一組目錄服務，包括尚未建立的目錄服務。</span><span class="sxs-lookup"><span data-stu-id="eaf73-112">In short, Active Directory Service Interfaces can provide access to a broad and diverse set of directory services — including those not yet built.</span></span>

<span data-ttu-id="eaf73-113">為了存取使用傳統 Api 的結構，ADSI 架構定義了低層級介面，不支援從 C 和 c + + 等語言存取的自動化。</span><span class="sxs-lookup"><span data-stu-id="eaf73-113">For access to structures that use traditional APIs, the ADSI architecture defines low-level interfaces that do not support Automation that are accessible from languages like C and C++.</span></span> <span data-ttu-id="eaf73-114">這些介面只是目錄服務的網路通訊協定的 COM 包裝函式。</span><span class="sxs-lookup"><span data-stu-id="eaf73-114">These interfaces are little more than COM wrappers for network protocols to a directory service.</span></span>

<span data-ttu-id="eaf73-115">將程式碼寫入已發行的介面，可讓您的應用程式連接到所有已安裝 ADSI 提供者的目錄服務，並整合所產生的資料。</span><span class="sxs-lookup"><span data-stu-id="eaf73-115">Writing code to the published interfaces allows your application to reach directory services for all installed ADSI providers and integrate the resulting data.</span></span> <span data-ttu-id="eaf73-116">只要稍微變更或完全不變更您的程式碼，您的應用程式就可以在安裝新的 ADSI 提供者時，繼續存取您網路上的其他目錄服務。</span><span class="sxs-lookup"><span data-stu-id="eaf73-116">With little or no changes to your code, your application can continue to access additional directory services on your network as new ADSI providers are installed.</span></span>

<span data-ttu-id="eaf73-117">下圖顯示 ADSI 如何融入應用程式環境。</span><span class="sxs-lookup"><span data-stu-id="eaf73-117">The following figure shows how ADSI fits into an application environment.</span></span> <span data-ttu-id="eaf73-118">無論應用程式是以 Visual Basic、C/c + +、VBScript、Microsoft JScript 開發系統，或是使用 Active Server Pages 的 web 應用程式所撰寫，Active Directory 服務介面都能讓您在不需要使用原生網路 Api 的情況下，對基礎目錄服務提供乾淨且簡單的存取權。</span><span class="sxs-lookup"><span data-stu-id="eaf73-118">Whether the application is written in Visual Basic, C/C++, VBScript, Microsoft JScript development system, or as a web application using Active Server Pages, Active Directory Service Interfaces provide a clean and easy-to-use access to the underlying directory services without having to use the native network APIs.</span></span>

![程式設計語言的 adsi 支援](images/ds2layr.png)

<span data-ttu-id="eaf73-120">如上圖所示，不支援 Automation 的用戶端可以存取所有 ADSI 介面，包括具有命名慣例的純 COM 介面 **IDirectoryXXX** ，以及具有命名慣例 **IADSXXX** 的 Automation com 介面。</span><span class="sxs-lookup"><span data-stu-id="eaf73-120">As shown in the preceding figure, clients that do not support Automation have access to all ADSI interfaces, including both pure COM interfaces with the naming convention **IDirectoryXXX** and Automation COM interfaces with the naming convention **IADsXXX**.</span></span> <span data-ttu-id="eaf73-121">由於用戶端主要是要求來自目錄服務的資訊，因此透過 OLE DB 和 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 的 ADSI 彈性查詢模型會有效。</span><span class="sxs-lookup"><span data-stu-id="eaf73-121">Because clients predominantly request information from directory services, the ADSI flexible query model through OLE DB and [**IDirectorySearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) is effective.</span></span>

 

 




