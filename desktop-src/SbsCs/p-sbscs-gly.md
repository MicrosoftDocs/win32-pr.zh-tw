---
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 9BC3D6A3-D8F5-42C6-9A68-68F1741207D7
title: 'P (隔離的應用程式和並存元件) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc8e3d2591cfa1544ce11045f95df42e4a27d39b4a2b40d09bc3f2c907c2abec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142011"
---
# <a name="p-isolated-applications-and-side-by-side-assemblies"></a>P (隔離的應用程式和並存元件) 

[B C](a-sbscs-gly.md) [D](d-sbscs-gly.md) E F [G](g-sbscs-gly.md) H [I](i-sbscs-gly.md) J K L [M](m-sbscs-gly.md) N O P Q [R](r-sbscs-gly.md) [S](s-sbscs-gly.md) T W X Y Z

<dl> <dt>

<span id="_win32_per_application_configuration_gly"></span><span id="_WIN32_PER_APPLICATION_CONFIGURATION_GLY"></span>**每個應用程式設定**
</dt> <dd>

可以覆寫特定元件的全域應用程式設定的設定。 每個應用程式的設定是由安裝在與可執行檔相同資料夾中的應用程式設定資訊清單檔所指定。 資訊清單檔案會描述應用程式所要使用之並存元件的版本或版本範圍。 當新版本的元件與應用程式不相容時，可能會使用每個應用程式設定。 在此情況下，可以針對特定並存元件覆寫應用程式的預設或全域設定。

</dd> <dt>

<span id="_win32_private_side_by_side_assembly_gly"></span><span id="_WIN32_PRIVATE_SIDE_BY_SIDE_ASSEMBLY_GLY"></span>**私用並存元件**
</dt> <dd>

私用並存元件只有指定的應用程式可以看見。 它會在本機安裝至隔離的應用程式，而元件的程式碼則會成為應用程式內容的私用。 私用並存元件的相依性會在應用程式資訊清單檔中描述。 私用並存元件可以用來抵消元件共用的負面影響，例如 DLL 衝突，以及簡化應用程式部署。

</dd> <dt>

<span id="_win32_public_key_token_gly"></span><span id="_WIN32_PUBLIC_KEY_TOKEN_GLY"></span>**公開金鑰 token**
</dt> <dd>

16字元的十六進位字串，表示用來簽署元件之公開金鑰的 SHA-1 雜湊最後8個位元組。 用來簽署目錄的公開金鑰必須是2048位或更高的版本。 所有共用並存元件的必要項。

</dd> </dl>

 

 



