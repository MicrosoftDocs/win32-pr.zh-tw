---
description: 如果您在64位電腦上提供計數器，如果您想要同時支援32位和64位的取用者，就必須在電腦上安裝32位和64位版本的提供者。
ms.assetid: 2dba2c46-0185-4ce6-a7cc-27cdd9b19b70
title: 64位支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e465529f35d8a9becb2583e9d5c00ac19a74d3be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978973"
---
# <a name="64-bit-support"></a>64位支援

64位效能資料提供者 DLL 無法在32位消費者進程中執行，而32位效能資料提供者 DLL 無法在64位進程中執行。 提供者註冊僅支援您的 `Library` 效能資料提供者 DLL 路徑的單一值，因此您無法提供32位取用者和64位取用者所使用的不同路徑。

下列選項可支援64位作業系統上的 V1 提供者：

- **建議：** 安裝並註冊提供者 DLL 32 位版本的路徑。
  - 32位的取用者會以原生方式運作：它們會將您的32位提供者 DLL 載入至32位取用者進程。
  - 64位的取用者會間接運作：它們無法將您的32位提供者 DLL 載入64位取用者進程，但是 Windows 會自動切換回建立32位的 perfhost 程式，將您的32位提供者 DLL 載入 perfhost 程式，並將效能資料從32位 perfhost 程式傳送至64位取用者進程。
- **僅限64位：** 安裝並註冊提供者 DLL 64 位版本的路徑。
  - 32位取用者將會失敗：無法將您的64位提供者 DLL 載入至32位進程。
  - 64位的取用者會以原生方式運作：它們會在同進程載入您的32位提供者 DLL。

> [!NOTE]
> 數個內建的 Windows 效能資料提供者會在中安裝32位 DLL `%systemroot%\syswow64` 、將64位 dll 安裝至 `%systemroot%\system32` ，並將 `Library` 路徑註冊為 `%systemroot%\system32\ProviderName.dll` ，以允許檔案系統重新導向將路徑解析為適當的 DLL。 只有屬於 Windows 作業系統一部分的效能資料提供者才支援此功能。 不屬於 Windows 作業系統的提供者不能將檔案安裝到 `Windows` 資料夾。 在 `Windows` 服務或升級期間，可能會移除資料夾中無法辨識的檔案。
