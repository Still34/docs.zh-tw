---
title: 如何：使用 Parallel.Invoke 執行平行作業
ms.date: 03/30/2017
ms.technology: dotnet-standard
dev_langs:
- csharp
- vb
helpviewer_keywords:
- task parallelism in .NET
- parallel programming, task parallelism
ms.assetid: 6b3ecd79-dec9-4ce1-abf4-62e5392a59c6
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: c0192e12c86b21eb126293bbd220e093b334768b
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/29/2018
ms.locfileid: "47455995"
---
# <a name="how-to-use-parallelinvoke-to-execute-parallel-operations"></a>如何：使用 Parallel.Invoke 執行平行作業

這個範例示範如何使用工作平行程式庫中的 <xref:System.Threading.Tasks.Parallel.Invoke%2A> 平行處理作業。 我們會對共用資料來源執行三項作業。 這些作業都不會修改來源，因此可以直接平行執行。

> [!NOTE]
> 本文件使用 Lambda 運算式來定義 TPL 中的委派。 如果您不熟悉 C# 或 Visual Basic 中的 Lambda 運算式，請參閱 [PLINQ 和 TPL 中的 Lambda 運算式](../../../docs/standard/parallel-programming/lambda-expressions-in-plinq-and-tpl.md)。

## <a name="example"></a>範例

[!code-csharp[TPL_Parallel#06](../../../samples/snippets/csharp/VS_Snippets_Misc/tpl_parallel/cs/parallelinvoke.cs#06)]
[!code-vb[TPL_Parallel#06](../../../samples/snippets/visualbasic/VS_Snippets_Misc/tpl_parallel/vb/parallelinvoke.vb#06)]

請注意，使用 <xref:System.Threading.Tasks.Parallel.Invoke%2A> 時，您只需指出要並行執行的動作即可，執行階段會處理所有執行緒排程詳細資料，包括自動根據主機電腦的核心數進行調整。

這個範例會平行處理作業，而不是資料。 除了前述方法以外，您也可以使用 PLINQ 來平行處理 LINQ 查詢，並依序執行查詢。 或者，您可以使用 PLINQ 來平行處理資料。 另一種方式是同時平行處理查詢和工作。 雖然產生的額外負荷可能會使處理器數目相對較少的主機電腦效能減低，但將更適用在具有較多處理器的電腦上。

## <a name="compile-the-code"></a>編譯程式碼

將整個範例複製並貼到 Microsoft Visual Studio 專案中，然後按 **F5** 鍵。

## <a name="see-also"></a>另請參閱

- [平行程式設計](../../../docs/standard/parallel-programming/index.md)
- [操作說明：取消工作及其子系](../../../docs/standard/parallel-programming/how-to-cancel-a-task-and-its-children.md)
- [平行 LINQ (PLINQ)](../../../docs/standard/parallel-programming/parallel-linq-plinq.md)
