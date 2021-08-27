---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 5591218A-3212-46D0-A40F-C0788B459545
title: " (隔離應用程式和並存元件) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10cc3f4efb5d43ab61de2b057f7501bed1c3fe7a79126a18f101e03ab9e21086
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127438"
---
# <a name="s-isolated-applications-and-side-by-side-assemblies"></a> (隔離應用程式和並存元件) 

[B C](a-sbscs-gly.md) [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O [P](p-sbscs-gly.md) Q [R](r-sbscs-gly.md) S T W X Y Z

<dl> <dt>

<span id="_win32_shared_side_by_side_assembly_gly"></span><span id="_WIN32_SHARED_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**共用並存元件**
</dt> <dd>

共用並存元件可供電腦上的多個應用程式使用。 它會安裝在 Windows 目錄的 Winsxs 資料夾中。 應用程式和系統管理員可以藉由指定應用程式設定，來管理要使用的共用元件的版本。 並存元件一律會伴隨資訊清單檔案，以提供有關元件的資訊給作業系統。

</dd> <dt>

<span id="_win32_side_by_side_assembly_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**並存元件**
</dt> <dd>

並存元件是一種 Win32 元件，隨附資訊清單。 並存元件包含一組資源（一組 Dll、windows 類別、COM 伺服器、類型程式庫或介面）的集合，這些資源一律會同時提供給應用程式。

</dd> <dt>

<span id="_win32_side_by_side_assembly_sharing_gly"></span><span id="_WIN32_SIDE_BY_SIDE_ASSEMBLY_SHARING_GLY"></span>**並存元件共用**
</dt> <dd>

使用並存元件以安全地在多個應用程式之間共用元件，以及抵銷共用的負面影響，例如 DLL 衝突。 並存元件共用會讓多個版本的 Win32 元件在系統上同時執行，而不是擁有單一版本的元件，而該元件會假設與所有應用程式的回溯相容性。 並存元件一律會伴隨提供元件資訊清單檔案的組件資訊清單檔，以將元件的相關資訊提供給作業系統。 應用程式和系統管理員可以在部署之後，藉由以全域或個別應用程式為基礎來更新應用程式設定，以管理並存元件共用。

</dd> </dl>

 

 



