---
description: 獨立軟體廠商 (Isv) 可以藉由註冊自己的已知資料夾，在系統上擴充已知的資料夾集。
ms.assetid: bb2c63e6-7525-4d20-ac50-591b3e53dea2
title: 如何使用自訂資料夾擴充已知資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3556b2e28664c63e7bc3b5fa28cf8696f679bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192686"
---
# <a name="how-to-extend-known-folders-with-custom-folders"></a>如何使用自訂資料夾擴充已知資料夾

獨立軟體廠商 (Isv) 可以藉由註冊自己的已知資料夾，在系統上擴充已知的資料夾集。 註冊之後，系統就會知道這些協力廠商資料夾。 [**IKnownFolderManager：： GetFolderIds**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-getfolderids)的任何呼叫都可以找到它們。 請注意，已知的資料夾必須是每部電腦的資料夾。 您無法建立每個使用者的已知資料夾。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

透過 [**KNOWNFOLDER \_ 定義**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-knownfolder_definition) 結構定義您的已知資料夾。

### <a name="step-2"></a>步驟 2:

透過呼叫 [**IKnownFolderManager：： RegisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-registerfolder)來註冊已知資料夾。

## <a name="remarks"></a>備註

如果您在安裝程式中為您的應用程式建立了已知資料夾，您也必須在卸載程式碼中包含 [**IKnownFolderManager：： UnregisterFolder**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iknownfoldermanager-unregisterfolder) 。

在註冊之前，請考慮您要將資料夾包含在已知資料夾系統中的原因。 您應具有將資料夾提升至該層級的系統可見度的有效理由。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[已知資料夾範例](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))
</dt> </dl>

 

 
