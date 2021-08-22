---
description: 由於 Winsock DLL 本身不再由每個個別堆疊廠商提供，因此堆疊廠商無法藉由將進入點新增至 Winsock DLL 來提供擴充功能。
ms.assetid: 5c71532a-c565-4f65-ab36-ca0e23190718
title: SPI 中的函數延伸機制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db2e5e32a4d79174893cfb2d9fa2ae0c0521a51ac80c40bcb6c45feab49693d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132421"
---
# <a name="function-extension-mechanism-in-the-spi"></a>SPI 中的函數延伸機制

由於 Winsock DLL 本身不再由每個個別堆疊廠商提供，因此堆疊廠商無法藉由將進入點新增至 Winsock DLL 來提供擴充功能。 為了克服這項限制，Winsock 利用新的 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式來容納希望提供提供者專屬功能延伸模組的服務提供者。 這項機制會 presupposes 應用程式知道特定的擴充功能，並瞭解相關的語法和語法。 服務提供者廠商通常會提供這類資訊。

若要叫用擴充功能，應用程式必須先要求所需函式的指標。 這是透過 [**WSAIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsaioctl) 函式使用 SIO 取得延伸模組函式 \_ \_ \_ \_ 指標命令程式碼來完成。 **WSAIoctl** 函式的輸入緩衝區包含所需擴充功能函式的識別碼，而且輸出緩衝區將包含函式指標本身。 然後，應用程式就可以直接叫用擴充功能，而不需透過 Ws2 \_32.dll。

指派給延伸模組函式的識別碼是由服務提供者廠商所配置 (Guid) 的全域唯一識別碼。 建立延伸模組函式的廠商呼籲，以發佈函式的完整詳細資料，包括函數原型的語法。 這可促進多個服務提供者提供的一般及/或熱門擴充功能。 應用程式可以取得函式指標並使用函式，而不需要知道任何有關執行函數的特定服務提供者。

 

 



