---
description: 當您完成類別或實例之後，您可能想要從 WMI 刪除該類別或實例。
ms.assetid: 8d4bf548-a332-4058-92d0-d613bbeaa408
ms.tgt_platform: multiple
title: 刪除類別或實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42a46a52400623e31df3e051a0b587f49326733b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192200"
---
# <a name="deleting-a-class-or-instance"></a>刪除類別或實例

當您完成類別或實例之後，您可能想要從 WMI 刪除該類別或實例。 如同其他物件導向技術，您可以刪除類別或實例物件來清除 WMI 命名空間，並傳回系統資源。 不過，WMI 中的許多類別和實例都是持續性的，而且在任何指定的時間都是由各種應用程式使用，因此在刪除 WMI 類別或實例時，您應該要特別小心：您的應用程式或其他應用程式可能會在稍後的日期需要類別或實例。

刪除類別或實例是一個簡單的程式。 不過，由於類別的永久本質，您可能不需要經常刪除某個類別。 例如，您不太可能刪除 [**Win32 \_ DiskDrive**](/windows/desktop/CIMWin32Prov/win32-diskdrive) 類別，因為您不太可能在企業中的某處沒有磁片磁碟機。 相反地，您會更有可能刪除類別的實例。 如需詳細資訊，請參閱 [刪除實例](deleting-an-instance.md)。

雖然很罕見，但您可能會在一段時間內需要更新所建立的類別。 例如，您可以建立類別來代表協力廠商應用程式。 如果協力廠商將其軟體更新至您的類別不再正確地表示軟體的範圍，您可能需要刪除原始類別。 如需詳細資訊，請參閱 [刪除類別](deleting-a-class.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設計受控物件格式 (MOF) 類別](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 
