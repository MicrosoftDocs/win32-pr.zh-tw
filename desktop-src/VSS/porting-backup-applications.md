---
description: Windows Server 2003 （含 Service Pack 1）的二進位檔 (SP1) 與 Windows Vista 和 Windows Server 2008 相容。 不過，必須重新編譯舊版 Windows 的二進位檔。
ms.assetid: ef40fdf6-b039-4664-bafb-b88c9286c010
title: 移植備份應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b85f052996e2c82b11f545bb604b0ed50a886420
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513133"
---
# <a name="porting-backup-applications"></a>移植備份應用程式

Windows Server 2003 （含 Service Pack 1）的二進位檔 (SP1) 與 Windows Vista 和 Windows Server 2008 相容。 不過，必須重新編譯舊版 Windows 的二進位檔。

## <a name="porting-windows-xp-backup-applications-to-windows-vista"></a>將 Windows XP 備份應用程式移植到 Windows Vista

自 Windows XP 起，有數個 VSS 介面已經變更。 Windows XP 應用程式至少必須使用來自 VSS 7.2 SDK 或 Windows Vista 或 Windows Server 2008 SDK 的標頭檔和程式庫重新編譯。

## <a name="porting-windows-server-2003-sp1-backup-applications-to-windows-vista"></a>將 Windows Server 2003 SP1 備份應用程式移植到 Windows Vista

Windows Server 2003 （含 SP1）中的二進位檔與 Windows Vista 和 Windows Server 2008 相容。 不過，大部分的 Windows Server 2003 SP1 備份應用程式都必須更新，以考慮新功能，如下列各節所述。

## <a name="compiling-backup-applications-for-windows-vista"></a>編譯適用于 Windows Vista 的備份應用程式

您可以使用 VSS 7.2 SDK 中提供的標頭檔和程式庫，來編譯使用 Windows Server 2003 中可用介面的應用程式。 若要使用新的介面，必須使用 Windows Vista SDK 隨附的標頭檔和程式庫重新編譯應用程式。

> [!Note]  
> 使用 Windows Vista 或 Windows Server 2008 編譯的二進位檔與 Windows Server 2003 SP1 或舊版 Windows 不相容。

 

 

 



