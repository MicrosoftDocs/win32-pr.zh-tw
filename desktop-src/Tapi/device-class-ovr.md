---
description: 裝置類別可讓程式設計人員以類似的方式來處理具有類似屬性的裝置，藉此簡化開發。
ms.assetid: 061f3037-1c71-4da1-88d7-29906c136d7b
title: '裝置類別 (TAPI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 560f95b40ffa34f5e02ee7857928b75425fc7ed5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944215"
---
# <a name="device-class"></a><span data-ttu-id="9f172-103">Device 類別</span><span class="sxs-lookup"><span data-stu-id="9f172-103">Device Class</span></span>

<span data-ttu-id="9f172-104">裝置類別可讓程式設計人員以類似的方式來處理具有類似屬性的裝置，藉此簡化開發。</span><span class="sxs-lookup"><span data-stu-id="9f172-104">Device classes simplify development by letting programmers treat devices that have similar properties in a similar manner.</span></span> <span data-ttu-id="9f172-105">例如，辦公室的數位電話通常比家中的標準話筒擁有更多功能，但是兩者的回應方式與基本的一組功能相同，而且兩者都屬於電話裝置類別。</span><span class="sxs-lookup"><span data-stu-id="9f172-105">For example, a digital phone in an office typically has more capabilities than a standard handset in a home, but both respond in much the same way to a basic set of functions, and both belong to a phone device class.</span></span> <span data-ttu-id="9f172-106">裝置類別可提供用來分類及支援新設備的架構，協助讓 TAPI 成為可擴充的。</span><span class="sxs-lookup"><span data-stu-id="9f172-106">Device classes help make TAPI extensible by providing a framework from which to classify and support new equipment.</span></span>

<span data-ttu-id="9f172-107">請參閱 tapi 已預先定義之類別的 [TAPI 裝置類別](./tapi-device-classes.md) 。</span><span class="sxs-lookup"><span data-stu-id="9f172-107">See [TAPI Device Classes](./tapi-device-classes.md) for classes that TAPI has predefined.</span></span> <span data-ttu-id="9f172-108">服務提供者可能會針對它所支援的設備，執行並定義其他裝置類別。</span><span class="sxs-lookup"><span data-stu-id="9f172-108">A service provider may implement and define additional device classes for the equipment it supports.</span></span> <span data-ttu-id="9f172-109">應用程式永遠不需要知道哪一個服務提供者會控制哪些裝置，但可能需要控制新裝置類別的資訊。</span><span class="sxs-lookup"><span data-stu-id="9f172-109">An application never needs to know which service provider controls which device, but may require information on the control of new device classes.</span></span>

<span data-ttu-id="9f172-110">服務提供者藉由將要求對應到實際的裝置命令來實作為裝置類別。</span><span class="sxs-lookup"><span data-stu-id="9f172-110">A service provider implements a device class by mapping requests into actual device commands.</span></span> <span data-ttu-id="9f172-111">例如，當 Hayes 相容數據機的服務提供者收到透過 TAPISVR 傳遞的命令以進行呼叫時，它會將傳統 AT 命令傳送到數據機。</span><span class="sxs-lookup"><span data-stu-id="9f172-111">For example, when the service provider for a Hayes-compatible modem receives a command passed through TAPISVR to make a call, it sends classic AT commands to the modem.</span></span>

<span data-ttu-id="9f172-112">服務提供者介面可以對應至各式各樣的環境，包括傳統上視為屬於電話語音的環境。</span><span class="sxs-lookup"><span data-stu-id="9f172-112">The service provider interface can be mapped to a wide range of environments, including those not traditionally thought of as belonging to telephony.</span></span> <span data-ttu-id="9f172-113">例如，透過以 IP 為基礎的網路（例如網際網路）的多媒體會議。</span><span class="sxs-lookup"><span data-stu-id="9f172-113">An example is multimedia conferencing over an IP-based network such as the Internet.</span></span>

<span data-ttu-id="9f172-114">應用程式開發人員應該牢記其他可能共用電話語音服務的應用程式。</span><span class="sxs-lookup"><span data-stu-id="9f172-114">Application developers should keep in mind the existence of other applications that may share telephony services.</span></span>

 

 
