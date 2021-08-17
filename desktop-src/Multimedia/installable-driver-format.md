---
title: 可安裝的驅動程式格式
description: 可安裝的驅動程式格式
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- 可安裝的驅動程式、格式
- 可安裝的驅動程式，DriverProc 函式
- 可安裝的驅動程式，訊息
- 驅動程式訊息
- 驅動程式格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c02f6bb2515d1f182146b84b7f0b971fa4b73fe2e2caf5abf63dfd4ddb272df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140787"
---
# <a name="installable-driver-format"></a>可安裝的驅動程式格式

每個可安裝的驅動程式都會匯出 [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) 函式。 這個常見的進入點函式會接收系統的 *驅動程式訊息* ，引導驅動程式執行動作或提供資訊。 當應用程式或 DLL 開啟或關閉驅動程式，或要求將訊息傳送至驅動程式時，系統會將驅動程式訊息傳送至 **DriverProc** 函式。 **DriverProc** 函式會處理訊息，或將訊息傳遞至預設的訊息處理常式，也就是 [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc)函數。 無論是哪一種情況， **DriverProc** 都必須傳回值，指出要求的動作是否成功。

 

 