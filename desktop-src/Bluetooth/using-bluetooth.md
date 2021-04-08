---
title: 使用藍牙
description: 本節說明與針對藍牙撰寫 Windows 應用程式相關的工作。
ms.assetid: a5eddf48-b548-44a8-ac09-ce16f8aa3943
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4b9b396de2635f9d1e76005c6638abb1d49c0ff
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "103684165"
---
# <a name="using-bluetooth"></a>使用藍牙

本節說明與針對藍牙撰寫 Windows 應用程式相關的工作。

藍牙提供 Ws2bth 和 BluetoothAPIs 檔案中的程式設計定義。 Bthsdpdef .h 檔案必須包含在 BluetoothAPIs 之前。 Ws2bth 必須包含在 Winsock2 之後，才能使用藍牙通訊端。 僅連結至 Bthprops，並避免連結至 Irprops .lib。 Irprops 只是為了回溯相容性而提供。 Bthprops 可在 Windows Vista SDK 中取得。 您可以使用 Windows Vista SDK 來開發 Windows XP Service Pack 2 (SP2) 的應用程式。 您可以從 [下載中心](https://download.microsoft.com/download/a/7/7/a7767f09-0136-4a96-a1f8-276bf0ee31fa/Setup.exe)取得 WINDOWS Vista SDK。

所有標準同步和重迭的機制，可讓您讀取和寫入目前支援其他位址系列的資料 \_ 。

SDK 隨附一些範例程式碼，可顯示使用 Winsock 2.2 和 RFCOMM 通訊協定的簡單藍牙應用程式。 您可以在 SDK 安裝位置的 C： \\ Program Files \\ Microsoft sdk \\ Windows \\ <version number> \\ 範例 \\ NetDs \\ winsock \\ Bluetooth 中找到範例的原始程式碼。

本節將說明下列主題。



| 區段                                                                                      | Content                                                                          |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| [使用 Windows 通訊端進行藍牙程式設計](bluetooth-programming-with-windows-sockets.md) | 說明如何使用 Windows 通訊端介面來執行藍牙網路。 |



 

 

 




