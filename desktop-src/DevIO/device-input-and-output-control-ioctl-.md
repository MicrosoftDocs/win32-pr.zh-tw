---
description: DeviceIoControl 函式會提供裝置輸入和輸出控制項 (IOCTL) 介面，讓應用程式可以直接與設備磁碟機進行通訊。
ms.assetid: 2dffd86a-162c-4e09-bfa1-73b87522741a
title: " (IOCTL) 的裝置輸入和輸出控制項"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce2bb2ee26c63c2aad02d8e8d167ff12383fc6b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847475"
---
# <a name="device-input-and-output-control-ioctl"></a> (IOCTL) 的裝置輸入和輸出控制項

[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)函式會提供裝置輸入和輸出控制項 (IOCTL) 介面，讓應用程式可以直接與設備磁碟機進行通訊。 **DeviceIoControl** 函式是一般用途的介面，可將控制程式代碼傳送至各種裝置。 每個控制項程式碼代表驅動程式要執行的作業。 例如，控制程式代碼可以要求設備磁碟機傳回對應裝置的相關資訊，或指示驅動程式在裝置上執行動作，例如將磁片格式化。

SDK 標頭檔中會定義一些標準控制項碼。 此外，設備磁碟機還可以定義自己的裝置特定控制項碼。 如需 SDK 檔中包含的標準控制代碼清單，請參閱 [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)的「備註」一節。

您可以指定的控制程式代碼類型取決於正在存取的裝置，以及您的應用程式執行所在的平臺。 應用程式可以使用標準控制代碼或裝置特定的控制碼，在磁片磁碟機、硬碟、磁帶機或 CD-ROM 光碟機上執行直接輸入和輸出作業。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[呼叫 DeviceIoControl](calling-deviceiocontrol.md)
</dt> </dl>

 

 
