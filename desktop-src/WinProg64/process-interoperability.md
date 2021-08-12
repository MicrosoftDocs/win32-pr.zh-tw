---
title: 進程互通性
description: 您可以使用模擬層，在64位 Windows 上執行以 Win32 為基礎的應用程式。 ARM 上的 Windows 10 包含 ARM64 的 x86 模擬層。 如需詳細資訊，請參閱執行32位應用程式。
ms.assetid: a573f26c-7577-4ff0-b314-ae0a33274738
keywords:
- 處理互通性 64-位 Windows 程式設計
- 互通性 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c74e75af4299e9c249ea46b8eac2cdd47de10eb3f832aa88d6b313d20304afc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561514"
---
# <a name="process-interoperability"></a>進程互通性

您可以使用模擬層，在64位 Windows 上執行以 Win32 為基礎的應用程式。 ARM 上的 Windows 10 包含 ARM64 的 x86 模擬層。 如需詳細資訊，請參閱執行 [32 位應用程式](running-32-bit-applications.md)。

在64位 Windows 上，64位進程無法載入32位動態連結程式庫 (DLL) 。 此外，32位進程無法載入64位 DLL。 但是，64位 Windows 支援遠端程序呼叫 (64 位和32位程式之間的 RPC)  (在同一部電腦上和跨電腦) 。 在64位 Windows 上，跨進程的32位 com 伺服器可以與64位用戶端通訊，而跨進程的64位 com 伺服器則可以與32位用戶端通訊。 因此，如果您有一個不是 COM 感知的32位 DLL，您可以將它包裝在跨進程 COM 伺服器，並使用 COM 將呼叫封送處理至64位進程。

同進程伺服器目前使用 **InprocServer** 登錄專案註冊。 在64位 Windows 上，64與32位的同進程伺服器應該使用 **InprocServer32** 專案。

如果通訊埠控制碼的本質是電腦的本機電腦，而且永遠不會使用在32位到64位界限上，請使用 **控制碼 \_ ptr** 類型，而不是 **INT \_ ptr** 或 **DWORD \_ ptr** 類型。 這包括將這類控制碼傳遞為 **DWORD** 值的移植 RPC 介面。 64位 **控制碼 \_ PTR** 是網路上的64位 (不會被截斷) ，因此不需要對應。  (32 位 **控制碼 \_ PTR** 是網路上的32位。 ) 

如需詳細資訊，請參閱 [設計與64位相容的介面](designing-64-bit-compatible-interfaces.md)。

 

 




