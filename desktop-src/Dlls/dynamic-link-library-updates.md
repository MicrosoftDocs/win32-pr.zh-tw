---
description: 有時需要以較新的版本取代 DLL。
ms.assetid: 82349a33-dc2c-4309-b0fc-890f230e3f2c
title: Dynamic-Link 程式庫更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a10f76103ddebc723466fb7e32a216c0c039691d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026385"
---
# <a name="dynamic-link-library-updates"></a>Dynamic-Link 程式庫更新

有時需要以較新的版本取代 DLL。 取代 DLL 之前，請先執行版本檢查，以確定您要以較新的版本取代舊版。 您可以取代使用中的 DLL。 您用來取代使用中 Dll 的方法，取決於您所使用的作業系統。 在 Windows XP 和更新版本中，應用程式應該使用 [隔離的應用程式和並存元件](/windows/desktop/SbsCs/isolated-applications-and-side-by-side-assemblies-portal)。

如果您執行下列步驟，就不需要重新開機電腦：

1.  使用 [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) 函式來重新命名要取代的 DLL。 請勿指定 \_ \_ 允許的 MOVEFILE 複製，並確認重新命名的檔案位於包含原始檔案的相同磁片區上。 您也可以將檔案命名為不同的擴充功能，以在相同的目錄中重新命名該檔案。
2.  將新的 DLL 複製到包含已重新命名之 DLL 的目錄。 所有應用程式現在會使用新的 DLL。
3.  使用 [**MoveFileEx**](/windows/desktop/api/winbase/nf-winbase-movefileexa) 搭配 MOVEFILE \_ 延遲 \_ 直到 \_ 重新開機，以刪除重新命名的 DLL。

在您進行這項取代之前，應用程式將會使用原始 DLL，直到卸載為止。 在您進行取代之後，應用程式將會使用新的 DLL。 當您撰寫 DLL 時，您必須小心確認它已準備好用於這種情況，特別是當 DLL 維持全域狀態資訊或與其他服務通訊時。 如果 DLL 未針對全域狀態資訊或通訊協定的變更做好準備，更新 DLL 將會要求您重新開機電腦，以確保所有應用程式都使用相同版本的 DLL。

 

 
