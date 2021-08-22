---
title: IAgentCommandsEx GetDefaultID
description: IAgentCommandsEx GetDefaultID
ms.assetid: 14079ae0-ad2c-4f38-9371-9914f8402e49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e4dabfb1c957031b353303775921a352bf40d984ac5de1ee9c933f79a5e02cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105224"
---
# <a name="iagentcommandsexgetdefaultid"></a>IAgentCommandsEx::GetDefaultID

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

``` syntax
HRESULT GetDefaultID(
   long * pdwID  // address of default command's ID
);
```

抓取 [**命令**](/windows/desktop/lwef/the-commands-collection-object) 集合中預設命令的識別碼。

-   傳回 \_ [確定] 表示作業成功。

<dl> <dt>

<span id="pdwID"></span><span id="pdwid"></span><span id="PDWID"></span>*pdwID*
</dt> <dd>

接收 [**命令**](/windows/desktop/lwef/the-command-object) 集之識別碼作為預設值的變數位址。

</dd> </dl>

這個屬性會傳回 [**命令**](/windows/desktop/lwef/the-commands-collection-object)集合中目前的預設 [**命令**](/windows/desktop/lwef/the-command-object)物件。 在字元的快顯功能表中，預設的命令為粗體。 不過，設定預設的命令不會變更命令處理或按兩下事件。

這個屬性只適用于您的用戶端應用程式使用的字元;此設定不會影響用戶端應用程式中其他字元或其他字元的用戶端。

## <a name="see-also"></a>另請參閱

[**IAgentCommandsEx::SetDefaultID**](iagentcommandsex--setdefaultid.md)


 

 