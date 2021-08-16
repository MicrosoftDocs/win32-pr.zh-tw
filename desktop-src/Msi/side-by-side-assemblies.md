---
description: 並存元件共用是一種基礎結構，用來執行下列作業：安全地在多個 applicationsOffset 之間共用元件。共用的負面影響，例如 DLL 衝突。
ms.assetid: ba73e7c3-a9d7-4cc3-b5ce-2483a594fcc0
title: 並存元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04f9a16d7002a107376f525dc73dea9f6df3e2f182cc84207d92bdbf0f37ce81
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628278"
---
# <a name="side-by-side-assemblies"></a>並存元件

並存元件共用是一種基礎結構，可用來執行下列作業：

-   安全地在多個應用程式之間共用元件
-   位移一些共用的負面影響，例如 DLL 衝突。

除了具有單一版本的元件（假設與所有應用程式的回溯相容性）之外，並存元件共用也可讓多個版本的 COM 或 Win32 元件在系統上同時執行。 如需詳細資訊，請參閱 [隔離的應用程式和並存元件](../sbscs/isolated-applications-and-side-by-side-assemblies-portal.md)。

並存元件可以安裝為 [共用元件](shared-assemblies.md) 或 [私用元件](private-assemblies.md)。

Windows XP 之前的系統無法使用並存元件。

 

 
