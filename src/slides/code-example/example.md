
<pre class="language-js fragment current-visible code-with-highlight" data-fragment-index="0" >
<code>
(function() {
  'use strict';
  angular.module('esign.components.ui.documents-list')

    .directive('snDocumentsList', function() {
      return {
        restrict: 'E',
        templateUrl: 'app/components/ui/documents-list/documents-list.part.html',
        scope: {},
        controllerAs: 'vm',
        bindToController: {
          documents: '=',
          select: '&'
        },
        <mark>controller: function() {</mark>
        }
      };
    });
})();
</code>
</pre>


<pre data-line="3-6" class="language-js fragment current-visible code-with-highlight" data-fragment-index="0">
<code>
(function() {
  'use strict';
  angular.module('esign.components.ui.documents-list')

    .directive('snDocumentsList', function() {
      return {
        restrict: 'E',
        templateUrl: 'app/components/ui/documents-list/documents-list.part.html',
        scope: {},
        controllerAs: 'vm',
        bindToController: {
          documents: '=',
          select: '&'
        },
        <mark>controller: function() {</mark>
        }
      };
    });
})();
</code>
</pre>


<pre data-line="6-10" class="language-js fragment current-visible" data-fragment-index="2" style="position:absolute;top:0;left:0;" >
<code>
(function() {
  'use strict';
  angular.module('esign.components.ui.documents-list')

    .directive('snDocumentsList', function() {
      return {
        restrict: 'E',
        templateUrl: 'app/components/ui/documents-list/documents-list.part.html',
        scope: {},
        controllerAs: 'vm',
        bindToController: {
          documents: '=',
          select: '&'
        },
        <mark>controller: function() {</mark>
        }
      };
    });
})();
</code>
</pre>